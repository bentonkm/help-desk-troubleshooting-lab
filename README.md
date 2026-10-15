\# Help Desk Troubleshooting Lab



\## Project Overview

This project demonstrates beginner-level IT support troubleshooting through simulated help desk tickets.



\## Objective

To practice identifying computer problems, investigating possible causes, documenting findings, and recommending solutions.



\## Tools Used

\- Windows 11

\- Task Manager

\- Windows Settings

\- Command Prompt

\- GitHub



\## Skills Practiced

\- Troubleshooting slow computers

\- Checking network connectivity

\- Checking available storage

\- Recording findings and solutions

\- Documenting help desk tickets



\## Help Desk Tickets



### Ticket #001: Computer Running Slowly

**Status:** Investigated

**Problem:**
A user reports that their computer is running slowly.

**Investigation:**
1. Opened Task Manager and checked CPU, memory, and disk usage.
2. Sorted processes by memory usage to identify applications using the most RAM.
3. Opened Windows Storage settings to check available disk space.

**Findings:**
- CPU usage was 10% in the initial screenshot.
- Memory usage was 55–56% during the investigation.
- Disk activity was 2% in the screenshots.
- Several applications were open simultaneously, including Firefox, Brave Browser, and Google Chrome.
- The computer had 313 GB of free storage out of 475 GB.
- Windows reported 24 GB of temporary files.

**Conclusion:**
The screenshots did not show unusually high overall resource usage or critically low storage. Multiple open applications may contribute to memory usage, but the root cause of the reported slowness has not been confirmed.

**Recommended Next Steps:**
- Ask the user when the slowdown occurs.
- Check whether the slowdown continues after restarting the computer.
- Investigate the temporary files before deciding whether cleanup is appropriate.

**Evidence:**
- `evidence/ticket-001/task-manager-processes.png`
- `evidence/ticket-001/memory-usage.png`
- `evidence/ticket-001/storage-usage.png`


### Ticket #002: Internet Connection Problem

**Status:** Investigated

**Problem:**
A user reports that their computer is connected to Wi-Fi but cannot access websites.

**Investigation:**
1. Ran `ipconfig` to check the computer's network configuration.
2. Ran `ping 192.168.100.1` to test communication with the router.
3. Ran `ping google.com` to test internet connectivity.
4. Ran `nslookup google.com` to test DNS resolution.

**Findings:**
- Wi-Fi IPv4 address: `192.168.100.45`
- Default gateway: `192.168.100.1`
- Router ping: 4 packets sent, 4 received.
- Google ping: 4 packets sent, 4 received.
- DNS lookup successfully returned IP addresses for `google.com`.

**Conclusion:**
The computer successfully communicated with the router and Google, and DNS resolution worked during testing. The basic network connection was working at the time of the investigation. The reported problem could not be reproduced during these tests.

**Recommended Next Steps:**
- Ask the user which websites are failing.
- Check whether the problem affects other devices.
- If the issue returns, investigate browser errors and network stability.

**Evidence:**
- `evidence/ticket-002/router-ping.png`
- `evidence/ticket-002/internet-ping.png`
- `evidence/ticket-002/dns-lookup.png`

### Ticket #003: Checking Available Storage

**Status:** Investigated

**Problem:**
A user reports that their computer may be running out of storage space.

**Investigation:**
1. Opened Windows Settings.
2. Navigated to System → Storage.
3. Checked total drive capacity, used space, free space, and storage categories.

**Findings:**
- Total drive capacity: 475 GB.
- Storage used: 162 GB.
- Free storage: 313 GB.
- Installed apps: 47.6 GB.
- Other files: 52.0 GB.
- System and reserved: 37.9 GB.
- Temporary files: 24.6 GB.

**Conclusion:**
The computer has 313 GB of free storage, so the drive is not close to being full. Windows reports 24.6 GB of temporary files that could be investigated before considering cleanup. No files were deleted during this investigation.

**Recommended Next Steps:**
- Ask the user what storage warning they received.
- Review temporary files and identify what can safely be removed.
- Obtain permission before deleting files or uninstalling applications.

**Evidence:**
- `evidence/ticket-003/storage-details.png`

- Task Manager can help identify applications using CPU and memory.
- High memory usage should be investigated before ending any processes.
- The `ipconfig` command displays network configuration.
- The `ping` command tests connectivity to another device or host.
- The `nslookup` command checks DNS resolution.
- Windows Storage settings help identify used and available disk space.
- Troubleshooting should be based on evidence rather than assumptions.
- Findings and recommended next steps should be documented clearly.
