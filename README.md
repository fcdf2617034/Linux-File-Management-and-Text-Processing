# Linux File Operations, Archiving & Text Processing Pipelines (WADF Module 1, Week 2)
**Course:** WADF-2026 – Web Application & Digital Forensics Fundamentals  
**Student Name:** Kenneth Ukata  
**Registration Number:** fcdf2617034  
**Environment:** Debian Linux (Kali Linux `kali@KENNETH`)  

---

## 📌 Lab Overview
This repository contains terminal logs, command executions, and evidence documentation for **WADF Module 1, Week 2 (Labs 3 & 4)**. The objective of this practical exercise was to advance command-line proficiency through structured workspace navigation, file modifications, interactive differential comparisons, safe deletion handling, multi-conditional advanced file searching (`find` vs. globs), archiving (`tar`, `gzip`), cryptographic integrity verification (`sha256sum`), and text-processing pipelines (`grep`, `awk`, `sed`)[cite: 78, 79, 80].

---

## 🛠️ Utilities & Concepts Covered
* **Workspace Verification & File Operations:** Validating directory structures, managing files, and performing interactive deletions and differential comparisons (`diff`)[cite: 78].
* **Advanced File Discovery:** Deploying multi-conditional `find` utilities based on file names, sizes, and modification timestamps, contrasting them against shell globbing wildcards[cite: 79].
* **Archiving, Compression & Checksums:** Packing directories into uncompressed archives (`tar`), compressing them with gzip (`.tar.gz`), generating SHA-256 integrity hashes (`sha256sum`), and testing extraction/recovery routines[cite: 80].
* **Text-Processing Pipelines:** Inspecting log files, writing regex matching queries, and stringing together text utilities (`grep`, `awk`) to parse user action summaries from access event logs[cite: 80].

---

## 📂 Key Practical Modules Covered

### Lab 3A & 3B: Workspace Verification & File Operations
* Verified directory tree structures and contents of `README.txt` within the project workspace[cite: 78].
* Executed interactive file modifications, compared states using `diff`, and handled safe deletion prompts[cite: 78, 79].

### Lab 3C: Advanced File Discovery (`find` vs. Globs)
* **Shell Globs (`*`, `?`):** Evaluated natively by the shell against files present in the immediate working directory.
* **`find` Utility:** Dynamically and recursively crawled directory hierarchies, evaluating real-time metadata constraints (size, modification time, type) independently of shell expansion[cite: 79].

### Lab 4A: Archiving, Compression & Integrity Validation
* Archived the workspace directory: `tar -cvf archive/week2_project.tar project/`[cite: 80]
* Compressed the archive using gzip: `gzip archive/week2_project.tar`[cite: 80]
* Generated a cryptographic checksum: `sha256sum archive/week2_project.tar.gz > archive/week2_project.tar.gz.sha256`
* Verified archive integrity and tested successful restoration workflows into a `restore-test` directory[cite: 80].

### Lab 4B: Text-Processing Pipelines & Log Parsing
* Inspected access event logs (`access_events.txt`) across working day directories[cite: 80].
* Used filtering and text extraction pipelines (`grep`, `awk`) to isolate specific access metrics and append summaries to `user_action_summary.txt`.

---

## 🔧 Troubleshooting & Practical Lessons Learned
* **Placeholder Syntax Error:** Encountered a *"No such file or directory"* error during command execution because angle brackets (`<>`) were literally typed into the command line around the registration number placeholder. Corrected by stripping the brackets and using raw alphanumeric strings.
* **Safe Preview Workflow:** Adopted the habit of using dry-run or listing patterns with wildcards prior to executing broad deletion or file-moving commands to preview exact target files safely.

---

## 💡 Key Takeaway & Reflection
> *"Stringing together core text-processing utilities to instantly summarize and parse system event logs demonstrated how efficient command-line data handling is for security auditing and forensic investigations."*
