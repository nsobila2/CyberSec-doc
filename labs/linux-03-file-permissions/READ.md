Linux 03: File Permissions Management
Overview
This project demonstrates my work as a cybersecurity analyst updating file permissions for a multimedia company’s research team. The projects directory contained files and directories with incorrect permissions, risking unauthorized access. Using Linux commands (ls, chmod) in a virtual machine, I checked and modified permissions to align with the organization’s security policies, ensuring least privilege. This project showcases Linux skills, access control practices, and professional documentation.
Contents

Permissions Guide: Detailed steps, commands, and outputs for checking and updating file and directory permissions.
[Future Work]: May include scripts for automating permission checks or additional Linux tasks.

Project Summary
The research team’s projects directory contained files and a directory with misconfigured permissions. I used ls -la to check permissions, interpreted the 10-character permission strings, and updated permissions using chmod to:

Remove write access for other on project_k.txt.
Restrict write access and ensure read access for user and group on the hidden file .project_x.txt.
Limit execute access to researcher2 on the drafts directory.

Methodology

Executed Linux commands in a virtual machine to check and modify permissions.
Analyzed permission strings to determine user, group, and other access levels.
Documented steps and outputs in Markdown for clarity and accessibility.

Learning Objectives

Master Linux commands (ls, chmod) for file permission management.
Apply least privilege principles to enhance system security.
Practice professional documentation using GitHub and Markdown.

Contact

