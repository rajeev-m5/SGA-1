# Question 2 Explanation

- Command: mkdir -p secure_workspace/{docs,src,logs} && touch ...  
  This created the requested directory structure and placeholder project files for the secure workspace.
- Command: ls -ld secure_workspace secure_workspace/*  
  This showed the initial permissions and confirmed the structure before changes were applied.
- Command: chmod 750 ... && chmod 640 ...  
  This restricted access so only the owner could manage the workspace while group members could read relevant files and others had no access.
- Command: stat -c ... && umask  
  This captured ownership details and the current umask value, which influences default permissions for newly created files.
