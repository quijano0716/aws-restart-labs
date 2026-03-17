# Agent Context & Project History

This file (`AGENTS.md`) is designed to provide context to any AI agent interacting with this repository. It details the project's purpose, what has been accomplished so far, the core rules, and the agent's role.

## Project Purpose
This project is dedicated to building a modern, static documentation site for **AWS re/Start Labs**. 
The goal is to convert raw materials (PDFs, markdown drafts, and screenshots) into fully polished, styled HTML lab reports that are easy to read and navigate.

## Agent Role: The Lab Builder
The AI agent acts as the primary "Lab Builder". Its core directive is to follow the `lab-builder` skill (located in `.agents/skills/lab-builder/SKILL.md`) to automate the creation of new labs. 

**Key responsibilities include:**
1. **Content Parsing:** Reading source materials such as `lab_drafts.md` and PDF guides to understand the lab's objective, commands, and workflow.
2. **PDF Conversion:** Running `node .agents/skills/lab-builder/scripts/convert_pdf.js` to extract text from PDFs when markdown sources are unavailable.
3. **Asset Management:** Creating lab directories under `docs/` and organizing screenshots into `assets/screenshots/` with descriptive names.
4. **HTML Generation:** Creating an `index.html` file for each lab that strictly follows the established structural and CSS template (originating from Lab 225).
5. **Index Updating:** Adding new lab cards to the main repository index (`docs/index.html`) to ensure all reports are easily accessible.
6. **Git Management:** Managing the git repository by staging changes and pushing to the remote `main` branch.

## What Has Been Completed So Far
*   **Infrastructure:** Created the custom `lab-builder` skill and structured the `.agents` folder. We updated `.gitignore` to prevent agent scripts and `node_modules` from cluttering the remote repository.
*   **Lab 11 (EC2):** Originally Lab 01, renamed to Lab 11.
*   **Lab 225 (Linux AMI):** Established the base CSS template and the specific SSH/PuTTY connection rules.
*   **Lab 227 (Linux CLI):** Created the report covering basic commands and command history.
*   **Lab 229 (Users & Groups):** Adapted the structure to use data tables for complex user assignments. 
*   **Lab 231 (Editing Files):** Documented the use of `vimtutor`, `vim`, and `nano`.
*   **Lab 233 (File System):** Documented folder creation and reorganization (`mkdir`, `cp`, `mv`, `rmdir`).
*   **Lab 235 (Working with Files):** Documented generating `tar` backups, logging with `echo`/`tee`, and transferring files.
*   **Version Control:** All these labs and their assets were successfully committed and pushed to the origin `main` repository branch.

## Critical Rules to Follow
1.  **NO Em Dashes:** Never use the em dash "—" in any generated content. Use standard hyphens "-", colons ":", commas ",", or parentheses `()` instead.
2.  **Writing Style:** Keep the tone strictly objective, direct, and professional. Avoid sensationalist language or unnecessary fluff.
3.  **SSH Instructions:** Detailed PuTTY/SSH setup instructions should only remain in Lab 225. Subsequent labs should simply reference Lab 225 for connection steps.
4.  **Windows Environment:** Terminal instructions and behaviors should expect a Windows environment for the local machine (e.g., using PuTTY, PowerShell).
5.  **Clean Code:** Do not minify the CSS inside the `index.html` files. Maintain readable, multi-line formatting.

---

*This document serves as the project's memory. Always review it when starting a new session or encountering ambiguity in the project's direction.*
