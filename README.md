# Windows Defender Firewall Configuration Task

This repository contains the documentation and output for configuring and testing Windows Defender Firewall rules on Windows 11, following the provided mini-guide. The task involves listing firewall rules, adding a rule to block port 23 (Telnet), testing the rule, adding a rule to allow port 22 (SSH, if applicable), removing the test rule, and documenting the process.

## Files
- `firewall_rules.txt`: Output of current firewall rules generated using PowerShell.
- `firewall_configuration.md`: Detailed documentation of steps, including GUI and PowerShell commands, and test results.
- `screenshots/` (optional): Folder containing screenshots of firewall rules and test results (e.g., `rules_list.png`, `test_telnet.png`).

## Instructions
1. Review `firewall_configuration.md` for a detailed step-by-step explanation of the process, including commands and GUI actions.
2. Check `firewall_rules.txt` for the list of Windows Defender Firewall rules at the time of the task.
3. View the `screenshots/` folder (if included) for visual confirmation of rules and test results.

## Environment
- **Operating System**: Windows 11
- **Tool**: Windows Defender Firewall with Advanced Security

## Notes
- All commands were executed with administrative privileges using PowerShell as Administrator.
- The Telnet client was enabled temporarily for testing port 23 and disabled afterward for security.
- The SSH rule (port 22) was optional, as Windows 11 does not include an SSH server by default. If not implemented, this is noted in `firewall_configuration.md`.
- Tests were performed locally; remote testing was skipped if no second device was available.
- Task performed on May 30, 2025, at 04:38 PM IST.

## How to Replicate
1. Open **Windows Defender Firewall with Advanced Security** or PowerShell as Administrator.
2. Follow the steps in `firewall_configuration.md` to list rules, add/test/remove rules, and document the process.
3. Use the PowerShell command `Get-NetFirewallRule | Format-Table -Property Name, DisplayName, Enabled, Direction, Action -AutoSize` to generate `firewall_rules.txt`.
