# Linux Security Operations and Git Practice

## Overview

A Kali Linux virtual machine project focused on Linux administration, Bash security auditing, and Git troubleshooting. The aim is to build practical skills for security operations while documenting the work and lessons learned.

## Linux account administration

I created a non-root working account and added it to the `sudo` group using `usermod -aG`. I verified its group membership with `groups paulwork`. This gave me practice with Linux users, group membership, and administrative access.

## Toolkit and practice areas

The project brief describes a Linux security toolkit with Bash scripts for:

- Reviewing user accounts, groups, sudo access, and UID 0 accounts.
- Checking services and processes.
- Inspecting listening ports and network connections.
- Reviewing authentication logs for failed SSH logins and sudo activity.
- Finding world-writable files and SUID/SGID binaries.

It also covers SSH key-based access, Git merge conflicts, rejected pushes, and recovering commits with `git reflog`.

## Evidence and next steps

The account and group commands above are supported by the terminal output shared for this project. The project discussion also described building scripts and resolving Git incidents, but the scripts, incident notes, and results have not yet been included here. Adding those artifacts will make it easier to show the work and explain the outcomes.

**Skills:** Kali Linux · User and group administration · sudo · Bash · Git · Security auditing
