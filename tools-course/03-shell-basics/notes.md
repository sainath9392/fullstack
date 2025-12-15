# Shell Basics Module Notes

## Safety Awareness (Drill 9)

### Why rm -rf is dangerous
`rm` stands for remove.
`-r` means recursive (deletes all files and subfolders inside a folder).
`-f` means force (does not ask for confirmation).
Running `rm -rf /` or `rm -rf .` can instantly delete your entire operating system or project without a way to undo it.

### Why avoid unnecessary sudo
`sudo` gives a command "root" (administrator) privileges.
1. It overrides safety checks.
2. It can change file permissions so that your normal user can no longer edit them.
3. If you run a malicious script with sudo, it has full control over your machine.

---

## Large Exercise: Mini Data Playground Findings

**Command used to generate data:**
`for i in {1..60}; do echo "Line $i: Status code $((RANDOM % 500))"; done > server_logs.csv`

**1. How many lines?**
Command: `wc -l server_logs.csv`
Result: 60

**2. How many contain the number "200"?**
Command: `grep "200" server_logs.csv | wc -l`
Result: [0]

**3. What are the first 5 lines?**
Command: `head -n 5 server_logs.csv`
Output:
[
Line 1: Status code 9
Line 2: Status code 250
Line 3: Status code 220
Line 4: Status code 7
Line 5: Status code 305
]

**4. What are the last 5 lines?**
Command: `tail -n 5 server_logs.csv`
Output:
[
Line 56: Status code 66
Line 57: Status code 20
Line 58: Status code 298
Line 59: Status code 102
Line 60: Status code 374
]
