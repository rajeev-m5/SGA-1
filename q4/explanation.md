# Question 4 Explanation

- Command: lsof | head -n 20  
  This listed active open files and helped identify processes using file descriptors.
- Command: exec 3<app.log && lsof -p $$  
  This opened the log file as file descriptor 3 and showed that the shell process had it open.
- Command: ls -l /proc/$$/fd  
  This exposed the kernel-managed file descriptor table and confirmed how the shell tracked open files.
- Command: ls -l > stdout.txt and ls /not_a_real_path 2> stderr.txt  
  These redirected standard output and standard error to separate files to show Linux I/O handling.
- Command: ulimit -a  
  This displayed the current resource limits that affect file descriptors, memory, and process usage.
