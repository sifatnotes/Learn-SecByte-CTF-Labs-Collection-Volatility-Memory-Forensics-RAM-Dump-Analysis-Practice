# Learn-SecByte-CTF-Labs-Collection-Volatility-Memory-Forensics-RAM-Dump-Analysis-Practice
A curated collection of hands-on cybersecurity CTF labs covering Volatility Memory Forensics, RAM Dump Collection, Process/DLL Enumeration, Injected Code Detection, Network Connection Analysis, and Rootkit Detection from Learn SecByte.
# Learn SecByte CTF & Cybersecurity Labs Collection

Welcome to the **Learn SecByte CTF & Cybersecurity Labs Collection**. This repository is a dedicated, searchable index of hands-on memory forensics, RAM capture triage, Volatility framework analysis, and behavioral malware investigation labs designed for cybersecurity students, CTF players, digital forensics & incident response (DFIR) specialists, SOC analysts, and threat hunters.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Volatile memory (RAM) contains critical forensic evidence that disappears upon system shutdown. Hosted on [Learn SecByte](https://learn.secbyte.org/), this collection of CTF challenge labs focuses on practical RAM dump acquisition and deep-dive volatile memory analysis.

From collecting physical memory dumps during live response incidents to leveraging the Volatility framework for process/DLL enumeration, inspecting open handles, extracting injected code payloads (`malfind`), tracing active/closed network connections (`netscan`), and detecting stealthy kernel rootkits, these exercises build job-ready DFIR capabilities.

---

## Lab Collection & Index

Below is the complete, searchable index of all memory forensics and RAM analysis challenges in this collection:

| # | Lab / Challenge Name | Category | Focus / Key Topics | Lab Link |
|---|----------------------|----------|---------------------|----------|
| 1 | **Rootkit Detection: Memory Forensics** | Rootkits & Kernel | System call table hooks, hidden kernel modules (`modules`/`modscan`), Ring 0 stealth | [Access Lab](https://learn.secbyte.org/ctf/rootkit-detection-memory-forensics) |
| 2 | **Injected Code Detection: Finding Malicious Logic in Trusted Drivers** | Code Injection | Memory allocation flags (`PAGE_EXECUTE_READWRITE`), `malfind`, VAD tree inspection | [Access Lab](https://learn.secbyte.org/ctf/injected-code-detection-finding-malicious-logic-in-trusted-d) |
| 3 | **Memory Artifact Extraction: From Volatile Clues to Case Resolution** | Memory Extraction | Memdumping injected processes, extracting unpacked PE payloads, artifact recovery | [Access Lab](https://learn.secbyte.org/ctf/memory-artifact-extraction-from-volatile-clues-to-case-resol) |
| 4 | **Network Connection Analysis: From Handshake to Hunt** | Network Forensics | `netscan` plugin, socket object analysis, C2 IP/port correlation, process mapping | [Access Lab](https://learn.secbyte.org/ctf/network-connection-analysis-from-handshake-to-hunt) |
| 5 | **Handle Analysis: From Dropper to Decoded Payload** | Process & Handles | Process handle tables (`handles`), open file handles, mutexes, registry keys | [Access Lab](https://learn.secbyte.org/ctf/handle-analysis-from-dropper-to-decoded-payload) |
| 6 | **DLL Enumeration Deep Dive** | Process & Modules | Loaded DLL lists (`dlllist`), unlinked DLLs (`ldrmodules`), shared object auditing | [Access Lab](https://learn.secbyte.org/ctf/dll-enumeration-deep-dive) |
| 7 | **Process Enumeration Recon Lab** | Process & Tree | Process tree carving (`pslist`, `pstree`, `psscan`), PPID relationships, orphan processes | [Access Lab](https://learn.secbyte.org/ctf/process-enumeration-recon-lab) |
| 8 | **Volatility Advanced Analysis: Memory Forensics** | Advanced Volatility | Custom Volatility plugins, KDBG structures, OS profile selection, memory pool carving | [Access Lab](https://learn.secbyte.org/ctf/volatility-advanced-analysis-memory-forensics) |
| 9 | **Volatility Fundamentals: Memory Forensics Essentials** | Volatility Basics | Volatility 2 & 3 syntax, profile identification (`imageinfo`/`banners`), basic triage | [Access Lab](https://learn.secbyte.org/ctf/volatility-fundamentals-memory-forensics-essentials) |
| 10 | **Memory Dump Analysis: The Sleeping Process** | Dynamic Memory | Process state inspection, thread analysis, suspended/sleeping execution triage | [Access Lab](https://learn.secbyte.org/ctf/memory-dump-analysis-the-sleeping-process) |
| 11 | **Memory Dump Collection: Incident Response Fundamentals** | Acquisition & Triage | WinPmem, FTK Imager CLI, live memory acquisition methods, dump integrity verification | [Access Lab](https://learn.secbyte.org/ctf/memory-dump-collection-incident-response-fundamentals) |
| 12 | **Behavioral Malware Analysis Lab** | Dynamic & RAM Triage | Sandbox execution alignment, runtime process monitoring, RAM artifact cross-correlation | [Access Lab](https://learn.secbyte.org/ctf/behavioral-malware-analysis-lab) |

---

## Categories

### 1. Volatility Framework Fundamentals & Acquisition
Master live memory capture methods and foundational Volatility syntax for parsing physical RAM dumps.
- [Memory Dump Collection: Incident Response Fundamentals](https://learn.secbyte.org/ctf/memory-dump-collection-incident-response-fundamentals)
- [Volatility Fundamentals: Memory Forensics Essentials](https://learn.secbyte.org/ctf/volatility-fundamentals-memory-forensics-essentials)
- [Volatility Advanced Analysis: Memory Forensics](https://learn.secbyte.org/ctf/volatility-advanced-analysis-memory-forensics)

### 2. Process, DLL & Handle Enumeration
Inspect running process trees, detect unlinked dynamic libraries, and audit system handles to uncover malicious artifacts.
- [Process Enumeration Recon Lab](https://learn.secbyte.org/ctf/process-enumeration-recon-lab)
- [DLL Enumeration Deep Dive](https://learn.secbyte.org/ctf/dll-enumeration-deep-dive)
- [Handle Analysis: From Dropper to Decoded Payload](https://learn.secbyte.org/ctf/handle-analysis-from-dropper-to-decoded-payload)
- [Memory Dump Analysis: The Sleeping Process](https://learn.secbyte.org/ctf/memory-dump-analysis-the-sleeping-process)

### 3. Code Injection, Payload Extraction & Network Forensics
Identify injected memory regions, extract malicious binaries directly from RAM, and map open network sockets to suspicious processes.
- [Injected Code Detection: Finding Malicious Logic in Trusted Drivers](https://learn.secbyte.org/ctf/injected-code-detection-finding-malicious-logic-in-trusted-d)
- [Memory Artifact Extraction: From Volatile Clues to Case Resolution](https://learn.secbyte.org/ctf/memory-artifact-extraction-from-volatile-clues-to-case-resol)
- [Network Connection Analysis: From Handshake to Hunt](https://learn.secbyte.org/ctf/network-connection-analysis-from-handshake-to-hunt)

### 4. Rootkits, Kernel Forensics & Behavioral Triage
Detect hidden kernel modules, system call hooks, and correlate volatile memory structures with dynamic behavior.
- [Rootkit Detection: Memory Forensics](https://learn.secbyte.org/ctf/rootkit-detection-memory-forensics)
- [Behavioral Malware Analysis Lab](https://learn.secbyte.org/ctf/behavioral-malware-analysis-lab)

---

## Learning Path

Follow this structured progression path to build job-ready digital forensics and volatile memory triage skills:

1. **Phase 1: Memory Acquisition & Volatility Basics** — Learn live RAM dumping techniques and initial image profiling:
   - [Memory Dump Collection: Incident Response Fundamentals](https://learn.secbyte.org/ctf/memory-dump-collection-incident-response-fundamentals)
   - [Volatility Fundamentals: Memory Forensics Essentials](https://learn.secbyte.org/ctf/volatility-fundamentals-memory-forensics-essentials)
   - [Behavioral Malware Analysis Lab](https://learn.secbyte.org/ctf/behavioral-malware-analysis-lab)

2. **Phase 2: Process, DLL & Handle Inspection** — Carve process trees, loaded modules, and open file handles:
   - [Process Enumeration Recon Lab](https://learn.secbyte.org/ctf/process-enumeration-recon-lab)
   - [DLL Enumeration Deep Dive](https://learn.secbyte.org/ctf/dll-enumeration-deep-dive)
   - [Handle Analysis: From Dropper to Decoded Payload](https://learn.secbyte.org/ctf/handle-analysis-from-dropper-to-decoded-payload)
   - [Memory Dump Analysis: The Sleeping Process](https://learn.secbyte.org/ctf/memory-dump-analysis-the-sleeping-process)

3. **Phase 3: Code Injection, Artifact Dumping & Network Analysis** — Locate injected VAD regions, dump binaries, and track C2 connections:
   - [Injected Code Detection: Finding Malicious Logic in Trusted Drivers](https://learn.secbyte.org/ctf/injected-code-detection-finding-malicious-logic-in-trusted-d)
   - [Memory Artifact Extraction: From Volatile Clues to Case Resolution](https://learn.secbyte.org/ctf/memory-artifact-extraction-from-volatile-clues-to-case-resol)
   - [Network Connection Analysis: From Handshake to Hunt](https://learn.secbyte.org/ctf/network-connection-analysis-from-handshake-to-hunt)

4. **Phase 4: Advanced Volatility & Kernel Rootkits** — Investigate low-level kernel hooks and custom memory structures:
   - [Volatility Advanced Analysis: Memory Forensics](https://learn.secbyte.org/ctf/volatility-advanced-analysis-memory-forensics)
   - [Rootkit Detection: Memory Forensics](https://learn.secbyte.org/ctf/rootkit-detection-memory-forensics)

---

## How to Use the Labs

1. Select a challenge link from the index or category sections above.
2. Read the scenario directives and download the memory dump files provided on [Learn SecByte](https://learn.secbyte.org/).
3. Utilize memory forensic platforms (Volatility 2, Volatility 3, MemProcFS, Rekall) and PE inspection tools (PEStudio, Ghidra) in an isolated forensic environment.
4. Execute plugins, locate anomalous memory regions, extract injected code, trace socket connections, and retrieve challenge flags.

---

## Disclaimer

This repository and its linked resources are strictly designed for educational, threat research, and authorized forensic training purposes. Never collect, analyze, or process volatile memory images containing sensitive production data without formal authorization.
