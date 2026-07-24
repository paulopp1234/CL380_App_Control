# CL380 App Control

Remote startup control for the CL380 LCD Production Tester.

The tester reads `status.txt` before its main window opens.

Use exactly one of these values:

- `ALLOW_START` — tester is allowed to open.
- `DO_NOT_START` — tester is blocked and exits.

The tester is intentionally fail-closed. If `status.txt` cannot be reached, GitHub is unavailable, the network is unavailable, or the file contains an unknown value, the tester does not start.

Current control URL:

`https://raw.githubusercontent.com/paulopp1234/CL380_App_Control/main/status.txt`
