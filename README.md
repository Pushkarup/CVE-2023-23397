# [CVE-2023-23397] Vulnerability Details 🚨💻
Microsoft has recently addressed a set of critical security vulnerabilities, including this zero-day exploits: CVE-2023-23397. The Common Vulnerability Scoring System (CVSS) assigned score of 9.8 to this exploit.

## CVE-2023-23397: Elevation of Privilege in Microsoft Outlook 📧🔓

A significant elevation of privilege (EoP) vulnerability has been identified in Microsoft Outlook. This flaw can have severe consequences as it enables attackers to exploit an Extended Messaging Application Programming Interface (MAPI) attribute containing a Universal Naming Convention (UNC) path in a malicious message. When the victim opens the message, the vulnerability triggers, directing them to an attacker-controlled Server Message Block (SMB) share on TCP port 445.

No user action is required to exploit this critical vulnerability. Upon connecting to the attacker's SMB server, the victim's New Technology LAN Manager (NTLM) negotiation message is automatically sent. The attacker can leverage this to authenticate on other systems supporting NTLM authentication. Notably, online services like Microsoft 365 remain unaffected as they do not support NTLM authentication.

### Technical Details 🛠️

**NTLM (New Technology LAN Manager):** NTLM is a hash used for authentication. Obtaining the NTLM hash allows lateral movement within the compromised network, posing a significant security risk.

**MAPI (Messaging Application Programming Interface):** MAPI provides developers with functions to create mail-enabled applications, offering control over the mail system on the client computer, including mail creation, mailbox management, and more.

**UNC (Universal Naming Convention):** UNC is a naming system in Windows identifying network resources. A UNC path comprises double backslashes (\) followed by the computer name or IP address hosting the resource.

### Affected Versions 🎯

The CVE-2023-23397 vulnerability impacts all currently supported versions of Microsoft Outlook for Windows, excluding Outlook for Android, iOS, or macOS. Microsoft recommends immediate patching to mitigate potential attacks.

Alternatively, if immediate patching is not feasible, Microsoft suggests adding users to the Protected Users group in Active Directory and blocking outbound SMB traffic on TCP port 445. These measures aim to minimize the impact of CVE-2023-23397.

### Active Exploitation 🌐🕵️

CERT-UA has reported this zero-day vulnerability to Microsoft, revealing active exploitation by threat actors associated with Russian intelligence services. Over the past year, these actors have targeted government, military, energy, and transportation organizations using this vulnerability.


# CVE-2023-23397 Exploit 🌐📧
<img width="464" alt="image" src="https://github.com/Pushkarup/CVE-2023-23397/assets/148672587/7e6092d3-a9c3-4e2b-b5a1-e1d6b37ac061">

## Description 🚀

This script exploits CVE-2023-23397, a vulnerability in Microsoft Outlook, allowing the generation of malicious emails for testing and educational purposes.

## Features ✨

- Generate malicious emails targeting Microsoft Outlook.
- Choose between saving the email as a .msg file or sending it directly.
- Menu-based user interaction for easy use.

## Prerequisites 🛠️

- Python 3.x 🐍
- Windows OS (due to the win32com.client dependency) 🖥️

## Usage 🚀

1. Clone the repository:

    ```bash
    git clone https://github.com/Pushkarup/CVE-2023-23397.git
    cd CVE-2023-23397
    ```

2. Install dependencies:

    ```bash
    pip install pywin32

    or
    
    pip install -r requirements.txt
    ```

3. Run the script:

    ```bash
    python Exploit.py
    ```

    Follow the on-screen prompts to enter the target email, attacker IP, and choose the action.

## Options ⚙️

- `save`: Save the malicious email as a .msg file.
- `send`: Send the malicious email.

## License 📝

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Disclaimer ⚠️

This script is intended for educational and testing purposes only. Use responsibly and only on systems you have explicit permission to test.

## Contributing 🤝

If you'd like to contribute to this project, please open an issue or create a pull request.

## Contact

- GitHub: [Pushkar Upadhyay](https://github.com/Pushkarup)
- LinkedIn: [Pushkar Upadhyay](www.linkedin.com/in/pushkar-upadhyay-24p)

## Donations
### Show your support
- BTC: 3QqVBBzDBezA9U77PCTwMPQVGb1eecv2SP
- ETH: 0xB779767483831BD98327A449C78FfccE2cc6df0a
- USDT: 0xB779767483831BD98327A449C78FfccE2cc6df0a


