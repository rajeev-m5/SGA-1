# Question 3 Explanation

- Command: ln original.txt hardlink.txt  
  This created a hard link, which points to the same inode as the original file.
- Command: ln -s original.txt symlink.txt  
  This created a symbolic link, which stores the path to the target file rather than sharing the inode.
- Command: ls -li and stat  
  These commands showed inode numbers and metadata, making the difference between hard links and symbolic links visible.
- Command: rm original.txt  
  This demonstrated that the hard link still worked because it preserved the file data, while the symbolic link became broken because it pointed to a deleted path.
