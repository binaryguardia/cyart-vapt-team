# Mobile Application Testing Lab

This lab focuses on Android application security testing using industry-standard tools to identify vulnerabilities through static and dynamic analysis.

---

## Objective
- Perform static and dynamic analysis of Android applications
- Identify insecure configurations and abused permissions
- Bypass security controls using runtime instrumentation
- Document findings in a professional security report format

---

## Tools Used
- **MobSF** – Static & Dynamic Analysis
- **Frida** – Runtime Hooking
- **Drozer** – IPC & Component Testing
- **Android Emulator / Test Device**

---

## Target Application
- Application Name: **Spotify (Mod APK)**
- File Type: APK
- Purpose: Security assessment for educational purposes

---

## Static Analysis (MobSF)

MobSF was used to perform static analysis on the Spotify Mod APK to identify insecure permissions, storage issues, and embedded libraries.

### Key Findings
- Excessive dangerous permissions
- Abused malware-related permissions
- Potential insecure storage access
- Third-party native libraries detected

### Evidence
Screenshots captured from MobSF static analyzer:
- Permissions analysis
- Abused permissions section
- Malware permission indicators

📸 **Screenshots**

<img width="1920" height="1080" alt="mobsf-3" src="https://github.com/user-attachments/assets/d4347072-3c79-45f7-aa77-e40431a405bd" />
<img width="1920" height="1080" alt="mobsf-2" src="https://github.com/user-attachments/assets/8826f953-1640-4fa2-9d11-2d0e41d87db5" />
<img width="1920" height="1080" alt="mobsf" src="https://github.com/user-attachments/assets/5673d446-8dd7-4a70-a04c-3efa0ada0978" />

---

## Static Analysis Log

| Test ID | Vulnerability       | Severity | Target App |
|--------:|---------------------|----------|------------|
| 016     | Insecure Storage    | High     | spotify_mod.apk |

---

## Dynamic Testing

### Frida – Runtime Hooking

Frida was used to hook application functions at runtime to analyze behavior and bypass security mechanisms such as authentication checks.

**50-Word Summary:**  
Frida was used to hook runtime functions of the Spotify Mod APK, allowing inspection and manipulation of authentication logic. This demonstrated how weak client-side controls can be bypassed dynamically, highlighting the importance of secure server-side validation and runtime protection mechanisms.

---

### Drozer – IPC & Component Testing
Drozer was used to test exported activities, services, and broadcast receivers to identify insecure IPC configurations and component exposure.

---

## Checklist (Documentation Reference)

The following checklist was maintained in Google Docs for tracking testing activities:

- [x] Run MobSF for static analysis  
- [x] Review permissions and malware indicators  
- [x] Hook functions using Frida  
- [x] Test IPC exposure using Drozer  
- [x] Capture screenshots and logs  
- [x] Document vulnerabilities and severity  

---

## Findings Summary

- High-risk permissions related to storage, audio, and device state
- Malware-like permission patterns detected
- Mod APK introduces additional security risks
- Runtime protections can be bypassed using dynamic instrumentation

---

## Conclusion

This lab demonstrates how modified Android applications can introduce serious security risks. Using MobSF, Frida, and Drozer provides deep visibility into app behavior, permissions abuse, and runtime weaknesses. Proper hardening, permission minimization, and anti-tampering controls are essential for secure mobile applications.

## Refrence
Mobsf: https://allabouttesting.org/quick-tutorial-mobsf-installation-on-linux-windows/

