# Project 1: Linux & Command Line Basics
**DecodeLabs Industrial Training Kit | Batch 2026**
**Role:** DevOps Engineer Intern

---

## Executive Summary
This project demonstrates foundational Linux command-line interface (CLI) operations required for DevOps environments. The objective is to manage directories, manipulate files, and inspect system structures without relying on graphical user interfaces (GUIs).

---

## Execution Log & Commands

Below is the terminal log demonstrating the completion of all core project requirements:

```bash
# 1. Create project root directory
mkdir Project-1

# 2. Navigate into project directory
cd Project-1

# 3. Create subdirectories for system organization
mkdir -p documentation logs scripts

# 4. Create empty placeholder files
touch documentation/readme.txt logs/app.log scripts/deploy.sh

# 5. Write metadata into documentation
echo "Project-1 - Linux Fundamentals" > documentation/readme.txt

# 6. Verify file contents
cat documentation/readme.txt

# 7. Inspect directory structure and permissions
ls -la