# Basic Digital Forensic Examination

## Project Overview

This project demonstrates a beginner-level digital forensic examination conducted in a Kali Linux virtual machine.

The exercise uses three self-created sample files to practise fundamental forensic examination techniques, including file identification, content inspection, SHA-256 hashing, hash verification and filesystem metadata examination.

**Project type:** Practical Digital Forensics Lab  
**Environment:** Kali Linux (VirtualBox)  
**Operating System:** Linux  
**Tools:** `file`, `cat`, `ls`, `sha256sum`, `stat`, `tree`

## Objectives

- Identify file types using Linux forensic utilities.
- Inspect the contents of sample files.
- Generate SHA-256 hashes.
- Verify file integrity using saved hash records.
- Examine filesystem metadata, permissions and timestamps.
- Document examination procedures, observations and limitations.

## Evidence Description

Three synthetic sample files were created for this exercise:

| File | Description | Size |
|---|---|---:|
| employee_list.csv | Sample employee records | 80 bytes |
| project_notes.txt | Sample project documentation | 92 bytes |
| reminder.txt | Sample investigation-related reminders | 114 bytes |

These files do not originate from an actual investigation.

## Examination Activities

### 1. File Type Identification
Used the Linux `file` command to identify the actual file types.

### 2. Content Inspection
Used the Linux `cat` command to inspect the contents of each sample file.

### 3. Evidence Inventory
Used the `ls -lh` command to record filenames, file sizes, ownership and permissions.

### 4. SHA-256 Hash Generation
Generated SHA-256 hashes for all three sample files and saved the results.

### 5. Hash Verification
Used `sha256sum -c` to verify that the current file contents matched the previously recorded hashes.

All three files returned an `OK` verification result.

### 6. Filesystem Metadata Examination
Used the Linux `stat` command to examine:
- File sizes
- File types
- Permissions
- Ownership
- Inode numbers
- Access, modification, change and birth timestamps

## Project Structure

```text
DFIR-Beginner-Project/
├── evidence/
│   ├── employee_list.csv
│   ├── project_notes.txt
│   └── reminder.txt
├── working/
├── hashes/
│   └── sha256_hashes.txt
├── screenshots/
│   ├── 01-file-type-identification.png
│   ├── 02-sha256-hash-generation.png
│   ├── 03-sha256-integrity-verification.png
│   └── 04-file-metadata-examination.png
└── report/
    └── examination_notes.txt
```

## Tools and Commands

| Tool | Purpose |
|---|---|
| `file` | File type identification |
| `cat` | Content inspection |
| `ls` | File inventory |
| `sha256sum` | Hash generation and verification |
| `stat` | Filesystem metadata examination |
| `tree` | Directory structure inspection |

## Limitations

- The sample files are synthetic and do not represent real-world evidence.
- Hash verification confirms consistency with the recorded hashes, not authenticity before initial hashing.
- Filesystem timestamps may be affected by file operations and system clock settings.
- File contents alone cannot establish authorship or the truth of the information recorded.

## Learning Outcomes

Through this exercise, I gained practical experience with fundamental digital forensic examination procedures, file integrity verification and forensic documentation using Linux command-line tools.

## Disclaimer

This project was created for educational and portfolio purposes. It does not contain real personal data or evidence from an actual investigation.
