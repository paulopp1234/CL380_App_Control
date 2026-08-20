# App Startup Control

Remote startup control for multiple applications.

Each application checks only its own control entry in `status.txt` before opening its main window.

Current entries:

- `ALLOW_START` — existing CL380 LCD Production Tester control.
- `OTMR CCF EDYTOR - ALLOW_START` — OTMR CCF Editor is allowed to open.

To block the OTMR CCF Editor, change only its line to:

- `OTMR CCF EDYTOR - DO_NOT_START`

The OTMR CCF Editor ignores the CL380 control line and uses only the line beginning `OTMR CCF EDYTOR - `.

The applications are intentionally fail-closed. If `status.txt` cannot be reached, GitHub/network access fails, the application's own line is missing, duplicated, or contains an unknown value, that application does not start.

Current control URL:

`https://raw.githubusercontent.com/paulopp1234/CL380_App_Control/main/status.txt`
