# Firewall Configuration 

## Environment
- **Operating System**: Windows 11
- **Firewall Tool**: Windows Defender Firewall with Advanced Security

## Steps Performed

### 1. Open Firewall Configuration Tool
- **GUI**: 
  - Pressed `Win + S`, typed **"Windows Defender Firewall with Advanced Security"**, and selected it.
  - This opened the Windows Defender Firewall management interface.
- **PowerShell**:
  - Opened PowerShell as Administrator via `Win + X` > **Windows PowerShell (Admin)**.

### 2. List Current Firewall Rules
- **GUI**:
  - In Windows Defender Firewall with Advanced Security, clicked **Inbound Rules** and **Outbound Rules** in the left pane.
  - Viewed the list of rules in the middle pane, noting details like Name, Enabled, Direction, and Action.
- **PowerShell**:
  - Command: `Get-NetFirewallRule | Format-Table -Property Name, DisplayName, Enabled, Direction, Action -AutoSize`
  - Saved output containing:
    ```powershell
    Get-NetFirewallRule | Format-Table -Property Name, DisplayName, Enabled, Direction, Action -AutoSize | Out-File firewall_rules.txt
