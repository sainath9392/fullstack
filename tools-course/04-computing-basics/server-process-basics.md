# Mini Server Investigation

## 1. The Setup
Started a server on port 5000.
Command: `python3 -m http.server 5000 &`

## 2. Investigation
**Finding the PID:**
Command used: `lsof -i :5000`
Result:
- **COMMAND:** python3
- **PID:** [6496]
- **USER:** [sainath]

## 3. Termination
**Stopping the server:**
Command: `kill 6496`

**Verification:**
Running `lsof -i :5000` returned nothing (port is free).
Browser failed to connect to localhost:5000.

## 4. Restart
Restarted server successfully on port 7000.