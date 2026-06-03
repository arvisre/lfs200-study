**Basic Concept 1** - In Linux systems, data is stored in Blocks. Each Block is 4KB in size. A single file can span over numerous data blocks.  
**Basic Concept 2** - Linux systems employ the concept of Index Nodes or inodes that are data structures containing metadata about files. Inodes are unique IDs assigned to each file in a filesystem.  

Using the command **stat** a user can find inode, block, and other information for a file.
<img width="834" height="269" alt="Screenshot From 2026-06-03 22-41-35" src="https://github.com/user-attachments/assets/38ee1e0a-09fb-41ab-a42c-d88654841980" />  
From the above image, we note the inode number **1573443**, the IO Block is 4096 or 4KB. The file is spread over 424 Blocks. The number of Blocks 424 * 512 bytes gives the size of the file.  

To find filesystem information, one can use the command **df** with the -h (human readable) -i (index node) and -T (type) options. See example below: 
<img width="1114" height="420" alt="Screenshot From 2026-06-03 23-00-05" src="https://github.com/user-attachments/assets/d9990cd8-cf05-48c8-bc6f-445cb60a601d" />  
One can note the Filesystem, type of Filesystem, the number of inodes, inodes users, inodes free, the size of each partition, and the mount point.  

The following image shows how two filesystems differ when it comes to size and inodes.  
<img width="599" height="189" alt="Screenshot From 2026-06-03 23-05-39" src="https://github.com/user-attachments/assets/991b9932-5b0f-4f74-9cdd-4b91ee7a4bc1" />  
The ext4 partition is 100 Gigabytes in size and has way too less inodes than an xfs partition that is 47 Gigabytes in size.






When a filesystem is created on a partition, the entire partition is broken down to Blocks. With ext4 partitions the inode table is pre-allocated during the time of partition.


