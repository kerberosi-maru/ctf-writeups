# SANS / ACT Now Veterans Day BootUp CTF (Nov 2026)

**Result:** 34th place, my first CTF
**Format:** 72-hour jeopardy-style CTF on Ranges.io (Nov 11–14, 2026). Ranking was by hit rate, so every wrong flag submission cost me, and verifying before submitting mattered as much as solving.

> This write-up covers skills and lessons only. There are no flags or step-by-step solutions, which keeps it fair for anyone running these challenges later.

## Categories I worked

| Category | Challenges solved | Skills used |
|---|---|---|
| Web / InvestiGate Portal | Multiple tasks in a shared web app | Directory enumeration (gobuster), recon, chaining small findings into admin access |
| Forensics | Data1, It's a Job, VB, Removed, Epoch, Corrupt 2, You're Getting Rich!, New Email | File-signature analysis, file repair, timestamp/epoch decoding, email and document artifacts, scripting triage |
| Mixed Offensive | .GGRX, Order Matters!, Super-ls, QR, Stickers | Encoding and obfuscation, Linux command-line tricks, QR and image analysis |
| SmartCity (group complete) | District Detour, Everyone Gets A Promotion, Crisis Room Eavesdropping | Abusing application logic, privilege escalation, traffic and comms interception |
| Truly Mixed | Don't Trust Me, EnCodEd, Endianess, A Byte or Not, Accruacy | Binary exploitation basics (stack overflows and byte order), disassembling ELF binaries, timing-based logic, data encoding and steganography |

I didn't finish **Sharks**, a packet-capture challenge. I got far enough to reverse a custom file-transfer protocol in the PCAP and carve out the files, but I ran out of time before I could fully rebuild the images. That one's on my list to finish.

## Tools
Kali Purple (VirtualBox), Python (pwntools-style scripting, `struct`, scapy, Pillow), `objdump`/`readelf`, gobuster, netcat, Wireshark, CyberChef-style decoding, and `strings`/hex inspection.

## Key lessons
1. **Verify before you submit.** With hit-rate scoring, a flag I'd checked locally was worth more than one I solved fast.
2. **Read the binary and don't guess.** Disassembling the program showed me exactly what condition it was checking, so I didn't have to brute-force blind.
3. **Byte order and encoding are everywhere.** Little-endian addresses, octal bytes, and reversed data came up again and again.
4. **Talking to a challenge service is free, but submitting isn't.** I tested freely against live services and only submitted when I was sure.
5. **Keep running notes.** A notes file I updated after every challenge kept me from repeating work across three days.
6. **Know when to park a challenge.** Moving on and coming back later beat burning hours on one problem.

## What's next
Finishing my MS in Computer Science, and doing more CTFs, with a focus on binary exploitation and network forensics on the way to AI/ML and cloud security.
