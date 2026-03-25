# Agent Context & Project History

This file (`AGENTS.md`) is designed to provide context to any AI agent interacting with this repository. It details the project's purpose, what has been accomplished so far, the core rules, and the agent's role.

## Project Purpose
This project is dedicated to building a modern, static documentation site for **AWS re/Start Labs**. 
The goal is to convert raw materials (PDFs, .docx guides, markdown drafts, and screenshots) into fully polished, styled HTML lab reports that are easy to read and navigate.

## Agent Role: The Lab Builder
The AI agent acts as the primary "Lab Builder". Its core directive is to follow the `lab-builder` skill (located in `.agents/skills/lab-builder/SKILL.md`) to automate the creation of new labs. 

**Key responsibilities include:**
1. **Content Parsing:** Reading source materials such as `lab_drafts.md`, PDF guides, and `.docx` files to understand the lab's objective, commands, and workflow. Use `mammoth` (`npx -y mammoth <file.docx> --output-dir=<dir>`) for `.docx` conversion.
2. **Screenshot Review:** Viewing each screenshot individually to determine its optimal placement within the lab report.
3. **Asset Management:** Creating lab directories under `docs/` and organizing screenshots into `assets/screenshots/` with descriptive names.
4. **HTML Generation:** Creating an `index.html` file for each lab that strictly follows the established structural and CSS template (originating from Lab 225).
5. **Index Updating:** Adding new lab cards to the main repository index (`docs/index.html`) to ensure all reports are easily accessible.
6. **Git Management:** Managing the git repository by staging changes and pushing to the remote `main` branch.

## What Has Been Completed So Far

### Batch 1: Compute + Linux Fundamentals (Labs 11 - 249)
*   **Lab 11 (EC2):** Introduction to Amazon EC2.
*   **Lab 225 (Linux AMI):** Introduction to Amazon Linux AMI. Established the base CSS template and the SSH/PuTTY connection rules.
*   **Lab 227 (Linux CLI):** Linux Command Line.
*   **Lab 229 (Users & Groups):** Managing Users and Groups.
*   **Lab 231 (Editing Files):** Editing Files.
*   **Lab 233 (File System):** Working with the File System.
*   **Lab 235 (Working with Files):** Working with Files.
*   **Lab 237 (Permissions):** Managing File Permissions.
*   **Lab 239 (Processes):** Managing Processes.
*   **Lab 241 (Monitoring):** Managing Services & Monitoring.
*   **Lab 243 (Software):** Software Management.
*   **Lab 245 (Log Files):** Managing Log Files.
*   **Lab 247 (Commands):** Working with Commands.
*   **Lab 249 (Bash Shell):** The Bash Shell.

### Batch 2: Networking (Labs 261 - 264)
*   **Lab 261 (Public/Private IPs):** Internet Protocols - Public and Private IP Addresses. Covered OSI model mapping to AWS, public vs. private IP differences, and VPC CIDR recommendations.
*   **Lab 262 (Static/Dynamic IPs):** Internet Protocols - Static and Dynamic Addresses. Covered dynamic IP behavior on EC2, Elastic IP allocation and association.
*   **Lab 263 (VPC Subnets):** Create Subnets and Allocate IP Addresses in a VPC. Covered CIDR planning, RFC 1918 private ranges, and VPC Wizard usage.
*   **Lab 264 (VPC Resources):** Create VPC Resources to Enable Internet Connectivity. Covered IGW, route tables, NACLs, security groups, EC2 launch, and ping verification.
*   **Landing Page:** Updated `docs/index.html` with a new Networking section containing all 4 lab cards.

### Upcoming: Batch 3
Source materials are ready in `ignoredocs/` for the following labs:
*   **Lab 251 (Bash Shell Scripts):** PDF + markdown guide + 4 screenshots in `ignoredocs/linux/251/`.

## Critical Rules to Follow
1.  **NO Em Dashes:** Never use the em dash "-" in any generated content. Use standard hyphens "-", colons ":", commas ",", or parentheses `()` instead.
2.  **Writing Style:** Keep the tone strictly objective, direct, and professional. Avoid sensationalist language or unnecessary fluff.
3.  **Lab Questions:** When labs include questions to answer, write responses that are concise, logical, and formally written. Avoid long paragraphs; use short, direct sentences that demonstrate understanding.
4.  **SSH Instructions:** Detailed PuTTY/SSH setup instructions should only remain in Lab 225. Subsequent labs should simply reference Lab 225 for connection steps.
5.  **Windows Environment:** Terminal instructions and behaviors should expect a Windows environment for the local machine (e.g., using PuTTY, PowerShell).
6.  **Clean Code:** Do not minify the CSS inside the `index.html` files. Maintain readable, multi-line formatting.
7.  **Adaptive Structure:** The standard lab template should be adapted per topic. For networking labs, custom elements like Q&A blocks, comparison panels, config cards, and data tables were added. Future batches may require similar adaptations.

---

*This document serves as the project's memory. Always review it when starting a new session or encountering ambiguity in the project's direction.*
