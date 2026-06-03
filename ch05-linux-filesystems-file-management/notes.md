**Basic Concept 1** - In Linux systems, data is stored in Blocks. Each Block is 4KB in size. A single file can span over numerous data blocks.  
**Basic Concept 2** - Linux systems employ the concept of Index Nodes or inodes that are data structures containing metadata about files. Inodes are unique IDs assigned to each file in a filesystem.  

Using the command **stat** a user can find inode, block, and other information for a file.
<img width="834" height="269" alt="Screenshot From 2026-06-03 22-41-35" src="https://github.com/user-attachments/assets/38ee1e0a-09fb-41ab-a42c-d88654841980" />  
From the above image, we note the inode number **1573443**, the IO Block is 4096 or 4KB. The file is spread over 424 Blocks. The number of Blocks 424 * 512 bytes gives the size of the file.
