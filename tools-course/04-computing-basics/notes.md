# Computing Basics Notes

## Identity
- **Current User:** `whoami` (Output: [sainath])
- **Home Dir:** `echo $HOME` (Output: /home/[sainath] or /Users/[sainath])

## Permissions
- **rwx:** Read, Write, Execute.
- **chmod +x:** Adds execute permission to a file, allowing it to run as a program.
- **Error:** "Permission denied" usually means you lack the 'x' permission on a script or 'w' permission on a folder.

## Ports & Processes
- **Port Conflict:** If I try to run two servers on port 3000, the second one fails with "Address already in use".
- **Fix:** Find the PID of the old process (`lsof -i :3000`) and kill it (`kill <PID>`).