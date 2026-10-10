---
title: Parameter Source Map
type: index
---

# Parameter Source Map

> **Pin this note in a sidebar** (Ctrl+click the tab in Obsidian) while writing
> new notes. When you need to know where a required parameter comes from,
> look it up here and copy the wikilink directly.
>
> **Faster alternative**: just type the wikilink-opening syntax in any note
> and Obsidian fuzzy-searches all notes, auto-completing the link for you.
> No need to memorize filenames or number prefixes.

---

## `hProcess (HANDLE — open handle to a remote process)`

**Produced by:**

- [[02. Get Remote Process Handle via CreateToolhelp32Snapshot.md]]
- [[04. Get Remote Process Handle via EnumProcesses.md]]
- [[06. Get Remote Process Handle via NtQuerySystemInformation.md]]
- [[01. Create a Suspended Process.md]]
- [[02. Create a Suspended Process via DEBUG_PROCESS.md]]

**Consumed by:**

- [[03. Remote Processs Injection via CreateRemoteThread]]
- [[02. Remote Shellcode Writing via VirtualAllocEx.md]]
- [[02. Remote Mapping Injection]]
- [[03. Remote DLL Injection via CreateRemoteThread]]

---

## `dwProcessId (DWORD — process ID of a remote process)`

**Produced by:**

- [[02. Get Remote Process Handle via CreateToolhelp32Snapshot.md]]
- [[04. Get Remote Process Handle via EnumProcesses.md]]
- [[06. Get Remote Process Handle via NtQuerySystemInformation.md]]
- [[01. Create a Suspended Process.md]]
- [[02. Create a Suspended Process via DEBUG_PROCESS.md]]

**Consumed by:**

- [[03. Get Remote Thread Handle via CreateToolhelp32Snapshot.md]]
- [[03. Remote APC Injection Early Bird via DEBUG_PROCESS]]

---

## `hThread (HANDLE — suspended/alertable thread for hijacking or APC)`

**Produced by:**

- [[01. Create a Suspended Process.md]]
- [[02. Create a Suspended Process via DEBUG_PROCESS.md]]
- [[02. Get Local Thread Handle via CreateToolhelp32Snapshot.md]]
- [[03. Get Remote Thread Handle via CreateToolhelp32Snapshot.md]]

**Consumed by:**

- [[01. Local Thread Hijacking via SetThreadContext]]
- [[02. Remote Thread Hijacking via SetThreadContext]]
- [[01. Local APC Injection via Alertable Thread]]
- [[02. Local APC Injection via Suspended Thread]]
- [[03. Remote APC Injection Early Bird via DEBUG_PROCESS]]
- [[04. Remote APC Injection Early Bird via Suspended Process]]

---

## `pAddress / ppAddress (PVOID — remote base address of injected payload)`

**Produced by:**

- [[02. Remote Shellcode Writing via VirtualAllocEx.md]]
- [[02. Remote Mapping Injection]]

**Consumed by:**

- [[02. Remote Thread Hijacking via SetThreadContext]]
- [[03. Remote APC Injection Early Bird via DEBUG_PROCESS]]
- [[04. Remote APC Injection Early Bird via Suspended Process]]

---

## `pPayload / pShellcode / pPlainTextData (PBYTE — raw payload buffer)`

**Produced by:**

- [[01. Read File from Disk.md]]
- [[01. Local Memory Management.md]]
- [[01. Payload Placement in .text Section.md]]
- [[02. Payload Placement in .rsrc Section.md]]
- [[03. Payload Staging Web Server via WinINet.md]]
- [[05. Read From Registry Key ASCII.md]]
- [[07. Read From Registry Key Unicode.md]]
- [[02. Shellcode IPv4Fuscation Deobfuscation.md]]
- [[04. Shellcode IPv6Fuscation Deobfuscation.md]]
- [[06. Shellcode MACFuscation Deobfuscation.md]]
- [[08. Shellcode UUIDFuscation Deobfuscation.md]]
- [[02. XOR Decryption Single-Byte Key.md]]
- [[04. XOR Decryption Index-Based Key.md]]
- [[06. XOR Decryption Repeating Key.md]]
- [[08. RC4 Payload Decryption Method 1.md]]
- [[10. RC4 Payload Decryption via SystemFunction032.md]]
- [[12. RC4 Payload Decryption via SystemFunction033.md]]
- [[14. AES Decryption via bCrypt.md]]
- [[16. AES Decryption via Tiny-AES.md]]

**Consumed by:**

- [[01. XOR Encryption Single-Byte Key.md]]
- [[03. XOR Encryption Index-Based Key.md]]
- [[05. XOR Encryption Repeating Key.md]]
- [[07. RC4 Payload Encryption Method 1.md]]
- [[09. RC4 Payload Encryption via SystemFunction032.md]]
- [[11. RC4 Payload Encryption via SystemFunction033.md]]
- [[13. AES Encryption via bCrypt.md]]
- [[15. AES Encryption via Tiny-AES.md]]
- [[01. Shellcode IPv4Fuscation Obfuscation.md]]
- [[03. Shellcode IPv6Fuscation Obfuscation.md]]
- [[05. Shellcode MACFuscation Obfuscation.md]]
- [[07. Shellcode UUIDFuscation Obfuscation.md]]
- [[01. Local Payload Execution via CreateThread]]
- [[02. Local Payload Execution via Function Pointer]]
- [[01. Local Thread Hijacking via SetThreadContext]]
- [[01. Local APC Injection via Alertable Thread]]
- [[02. Local APC Injection via Suspended Thread]]
- [[01. Callback Code Execution]]
- [[01. Local Mapping Injection]]
- [[03. Remote Processs Injection via CreateRemoteThread]]
- [[02. Remote Shellcode Writing via VirtualAllocEx.md]]
- [[02. Remote Mapping Injection]]

---

## `pKey (PBYTE — encryption/obfuscation key)`

**Produced by:**

- [[04. Generate Random Byte Key.md]]

**Consumed by:**

- [[05. XOR Encryption Repeating Key.md]]
- [[07. RC4 Payload Encryption Method 1.md]]
- [[09. RC4 Payload Encryption via SystemFunction032.md]]
- [[11. RC4 Payload Encryption via SystemFunction033.md]]
- [[13. AES Encryption via bCrypt.md]]
- [[15. AES Encryption via Tiny-AES.md]]

---

## `pCipherTextData (PBYTE — encrypted payload buffer)`

**Produced by:**

- [[13. AES Encryption via bCrypt.md]]
- [[15. AES Encryption via Tiny-AES.md]]

**Consumed by:**

- [[14. AES Decryption via bCrypt.md]]
- [[16. AES Decryption via Tiny-AES.md]]

---

## `Ipv4Array / Ipv6Array / MacArray / UuidArray (CHAR*[] — obfuscated shellcode as string array)`

**Produced by:**

- [[01. Shellcode IPv4Fuscation Obfuscation.md]]
- [[03. Shellcode IPv6Fuscation Obfuscation.md]]
- [[05. Shellcode MACFuscation Obfuscation.md]]
- [[07. Shellcode UUIDFuscation Obfuscation.md]]

**Consumed by:**

- [[02. Shellcode IPv4Fuscation Deobfuscation.md]]
- [[04. Shellcode IPv6Fuscation Deobfuscation.md]]
- [[06. Shellcode MACFuscation Deobfuscation.md]]
- [[08. Shellcode UUIDFuscation Deobfuscation.md]]

---

## `Text_RawData (const unsigned char[] — payload embedded in .text section)`

**Produced by:**

- [[01. Payload Placement in .text Section.md]]

**Consumed by:**

- [[01. Callback Code Execution]]

---

## `pFileBuffer / ppFileBuffer (PBYTE — file content read from disk)`

**Produced by:**

- [[01. Read File from Disk.md]]

**Consumed by:**

- [[02. Write File to Disk.md]]

---

## How to use this map

### When writing a NEW note
1. Write the technique's description, usage, code, and example as usual.
2. Look at the function's input parameters (the `IN ...` args).
3. For each parameter, find it in this map.
4. Under **Produced by**, copy the wikilink(s) into your note's
   `**Parameter Sources**` section.
5. If the parameter isn't listed here, just **skip that parameter** —
   don't write anything for it. Only list parameters that have a real
   source note.

### When adding a note that PRODUCES a new parameter
1. Add the note to the appropriate category folder.
2. Open this map and add the new note under the parameter's **Produced by** list.
3. Check if any existing notes consume that parameter — if so, add the
   wikilink to their `**Parameter Sources**` section.

### Quick tip — Obsidian autocomplete
Type the wikilink-opening syntax in any note. Obsidian shows a fuzzy-search
dropdown of all notes. Type 2-3 letters of the technique name and press Enter.
The link is inserted automatically with the correct filename. You never need
to type the full filename or remember the number prefix.
