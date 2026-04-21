# Blue - TryHackMe Writeup

## Machine Info
- Platform: TryHackMe
- OS: Windows 7 Professional SP1
- Difficulty: Easy

## Enumeration
### Nmap Scan
[paste your nmap output here]

### Key Findings
- Port 445 open (SMB)
- Windows 7 SP1 — potential MS17-010

## Vulnerability Identification
### MS17-010 Confirmation
[paste smb-vuln-ms17-010 nmap output]

## Exploitation
### EternalBlue (MS17-010)
- Module used: exploit/windows/smb/ms17_010_eternalblue
- Result: NT AUTHORITY\SYSTEM shell directly

## Post Exploitation
### Flag Locations
- Flag 1: C:\flag1.txt
- Flag 2: C:\Windows\System32\config\flag2.txt
- Flag 3: C:\Users\Jon\Documents\flag3.txt

## Key Learnings
- Windows 7 + Port 445 = always check MS17-010
- EternalBlue is a kernel exploit — lands directly as SYSTEM
- .rb files = Metasploit modules
