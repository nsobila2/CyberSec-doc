Linux File Permissions Management Guide
This guide documents the steps I took as a cybersecurity analyst to update file permissions in the projects directory for a multimedia company’s research team. Using Linux commands in a virtual machine, I checked existing permissions, interpreted permission strings, and modified access to align with security policies, ensuring least privilege.
Step 1: Check File and Directory Details
Objective: Determine existing permissions for files and directories in the projects directory.

Command:ls -la


Explanation: The ls -la command lists all contents, including hidden files, with detailed permissions. The output shows one directory (drafts), one hidden file (.project_x.txt), and five project files (project_k.txt, project_m.txt, project_p.txt, project_t.txt, project_z.txt).
Sample Output:drwxr-xr-x 2 researcher2 research 4096 Oct 10 2025 drafts
-rw-rw-r-- 1 researcher2 research  123 Oct 10 2025 project_k.txt
-rw-rw-r-- 1 researcher2 research  456 Oct 10 2025 project_m.txt
-rw-rw-r-- 1 researcher2 research  789 Oct 10 2025 project_p.txt
-rw-rw-r-- 1 researcher2 research  234 Oct 10 2025 project_t.txt
-rw-rw-r-- 1 researcher2 research  567 Oct 10 2025 project_z.txt
-rw-rw-r-- 1 researcher2 research  101 Oct 10 2025 .project_x.txt



Step 2: Describe the Permissions String
Objective: Interpret the 10-character permission string to understand access levels.

Permission String Breakdown:
1st character: File type (d for directory, - for regular file).
2nd-4th characters: User permissions (read, write, execute; - for no permission).
5th-7th characters: Group permissions (r, w, x; - for no permission).
8th-10th characters: Other permissions (r, w, x; - for no permission).


Example: For project_t.txt (-rw-rw-r--):
-: Regular file.
rw-: User has read and write permissions, no execute.
rw-: Group has read and write permissions, no execute.
r--: Other has read permission only.



Step 3: Change File Permissions
Objective: Remove write access for other on project_k.txt.

Commands:chmod o-w project_k.txt
ls -la


Explanation: The chmod o-w command removes write permission for other on project_k.txt. The ls -la command verifies the change.
Updated Output:-rw-rw-r-- 1 researcher2 research  123 Oct 10 2025 project_k.txt

After change:-rw-rw-r-- 1 researcher2 research  123 Oct 10 2025 project_k.txt

(Note: The original output already shows r-- for other, suggesting write was not present. This step ensures compliance.)

Step 4: Change Permissions on a Hidden File
Objective: Ensure .project_x.txt has no write access for anyone, with read access for user and group.

Commands:chmod u-w,g-w,g+r .project_x.txt
ls -la


Explanation: The chmod u-w,g-w,g+r command removes write permissions for user and group, and adds read permission for group. The ls -la command verifies the change.
Updated Output:-rw-rw-r-- 1 researcher2 research  101 Oct 10 2025 .project_x.txt

After change:-r--r--r-- 1 researcher2 research  101 Oct 10 2025 .project_x.txt



Step 5: Change Directory Permissions
Objective: Restrict drafts directory access to researcher2 only, removing execute permissions for group and other.

Commands:chmod g-x,o-x drafts
ls -la


Explanation: The chmod g-x,o-x command removes execute permissions for group and other on the drafts directory, ensuring only researcher2 has access. The ls -la command verifies the change.
Updated Output:drwxr-xr-x 2 researcher2 research 4096 Oct 10 2025 drafts

After change:drwx------ 2 researcher2 research 4096 Oct 10 2025 drafts



Summary
I updated permissions in the projects directory to align with the organization’s security policies:

Checked permissions using ls -la.
Removed write access for other on project_k.txt.
Configured .project_x.txt to have read-only access for user and group.
Restricted drafts directory access to researcher2 only.These changes enforce least privilege, reducing unauthorized access risks.

Contact
