# Automated-Disk-Sanitizer

## 🚀 Overview
Automated Disk Sanitiser is a Python-based storage optimization and cleanup system designed for efficient data deduplication. It acts as an intelligent file scanner that recursively traverses a target directory, identifies duplicate files by verifying their actual content hashes, and safely purges redundant copies while preserving a single original.  

## ✨ Key Features
* Content-Based Deduplication: Uses MD5 hashing to generate unique digital fingerprints, ensuring accurate identification even if duplicate files have been renamed.
* Chunk-by-Chunk Processing: Reads files in optimized 1000-byte streams to maintain a low memory footprint when scanning large media or document files.
* Recursive Directory Traversal: Deep-scans complex folder structures and subdirectories automatically using os.walk.
* Binary-Safe Stream Handling: Opens files in binary read mode ("rb"), making it perfectly safe for analyzing diverse formats like images, PDFs, videos, and binaries.
* Automated Redundancy Purging: Filters data groups to isolate redundancies, keeping the first discovered copy intact while deleting subsequent clones via os.remove.  

##🛠 Tech Stack
* Language: Python
* Core Modules: hashlib — For creating unique MD5 checksum fingerprints.
* os — For directory pathing, structure validation, and permanent disk deletion.  
