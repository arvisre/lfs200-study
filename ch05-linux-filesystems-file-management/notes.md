**Basic Concept 1** - In Linux systems, data is stored in Blocks. Each Block is 4KB in size. A single file can span over numerous data blocks.  
**Basic Concept 2** - Linux systems employ the concept of Index Nodes or inodes that are data structures containing metadata about files. Inodes are unique IDs assigned to each file in a filesystem.  

Using the command **stat** a user can find inode, block, and other information for a file.
