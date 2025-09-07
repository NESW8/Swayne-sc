# Windows Fundamentals 1 - TryHackMe

## 📌 Overview
This room is the first part of the Windows Fundamentals series on TryHackMe.  
It introduces the basics of the **Windows operating system**, including the desktop, NTFS file system, UAC, the Control Panel, and more.

---

## 🖼️ Progress Screenshot
![Room Completion](65e4a7b0-96f2-4876-aa57-d07e22e95449.png)

---

## ✅ Tasks

### Task 1 - Introduction to Windows
- Learned about the Windows operating system (OS), its utilities, files, settings, and features.  
- Connected to the Windows VM via RDP with given credentials.

---

### Task 2 - Windows Editions
- Windows versions: XP, Vista, 7, 8.x, 10, 11.
- Current desktop OS: **Windows 11** (Pro & Home editions).  
- Server OS: **Windows Server 2025**.  
- Key difference: **BitLocker encryption** is available on **Pro**, not on **Home**.

---

### Task 3 - The Desktop (GUI)
- GUI components:  
  1. Desktop  
  2. Start Menu  
  3. Search Box  
  4. Task View  
  5. Taskbar  
  6. Toolbars  
  7. Notification Area  
- Customization: display settings, personalization (themes, wallpaper).

---

### Task 4 - The File System
- Windows uses **NTFS (New Technology File System)**.  
- Features:  
  - Supports files > 4GB  
  - File/folder compression  
  - Permissions (Full control, Modify, Read/Execute, List, Write, Read)  
  - Journaling and recovery  
  - Encryption (EFS)  
- Special feature: **ADS (Alternate Data Streams)** – can be abused by malware to hide data.

---

### Task 5 - System32 Folders
- `C:\Windows` folder contains the operating system.  
- `C:\Windows\System32` holds critical OS files.  
- Environment variable: **%windir%**.

---

### Task 6 - User Accounts, Profiles, and Permissions
- Two account types: **Administrator** & **Standard User**.  
- User profiles stored under: `C:\Users`.  
- Checked groups via `lusrmgr.msc`.  
- Built-in accounts: **Guest** (disabled by default).

---

### Task 7 - User Account Control (UAC)
- Purpose: prevents programs from running with elevated privileges without user confirmation.  
- Protects against malware.  
- Shown by a **shield icon** on executable files.  

---

### Task 8 - Settings and the Control Panel
- Control Panel views: Category, Large icons, Small icons.  
- Small icons → last setting: **Windows Defender Firewall**.  
- Taskbar settings allow hiding/disabling:  
  - Search box (`Hidden`)  
  - Task View button (`Show Task View button` unchecked).  

---

### Task 9 - Task Manager
- Shortcut: **Ctrl + Shift + Esc**.  
- Provides info about: running apps, background processes, performance, startup apps, users.  

---

### Task 10 - Conclusion
- Learned the fundamentals of:  
  - Windows OS editions  
  - GUI navigation  
  - File system (NTFS & ADS)  
  - System32 importance  
  - Accounts & permissions  
  - UAC security  
  - Control Panel settings  
  - Task Manager usage  

---

## 🎯 Key Takeaways
- **BitLocker** → Only on Pro edition.  
- **NTFS** → Default Windows file system with advanced features.  
- **UAC** → Protects against unauthorized elevation.  
- **Ctrl+Shift+Esc** → Direct shortcut to Task Manager.  
- **%windir%** → System environment variable for Windows folder.  

---

## 🖼️ Additional Screenshots
Below are the screenshots captured during the room:

![Task 1](c60e7080-3556-402b-bb19-c7ac7fc06030.png)  
![Task 2](ad08e4e5-2f41-474a-9882-c08558886f47.png)  
![Task 3](353b1a46-8eb6-4b03-809d-52f8e7945597.png)  
![Task 4](1e902606-8e40-4dc8-b6ca-452a3bcc5036.png)  
![Task 5](4fb15fb3-55cd-47eb-8cbf-79b33ccfbd83.png)  
![Task 6](33297a41-8d4a-4d13-840b-8505cc1d284e.png)  
![Task 7](b424cacf-c379-4ee4-95e8-ebf337ebcf23.png)  
![Task 8](ac5fdbfb-1241-4bdf-93aa-a737ed2a8cba.png)  
![Task 9](a238323f-0eef-4e22-a1b0-22846fe1c414.png)  
![Task 10](60e45482-321f-43e9-9d41-2648a7df96a6.png)  

---

## 📂 Room Completed
- Status: ✅ **100% completed**  
- Room: **Windows Fundamentals 1**  
