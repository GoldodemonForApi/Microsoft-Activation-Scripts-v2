<p align="center"><img src="https://massgrave.dev/img/logo_small.png" alt="MAS Logo"></p>

<h1 align="center">Microsoft  Activation  Scripts (MAS)</h1>

<p align="center">Open-source Windows and Office activator featuring HWID, Ohook, TSforge, and Online KMS activation methods, along with advanced troubleshooting.</p>

<hr>
  
## How to Activate Windows / Office / Extended Security Updates (ESU)?

### Method 1 - PowerShell ❤️

1. Click the **Start Menu**, type `PowerShell`, and open it.

2. Copy and paste the code below and press **Enter.**  
   - For **Windows 8.1, 10 and 11**:
     ```
     irm https://get.activated.win | iex
     ```
	 If the above is blocked (by ISP/DNS), try this (needs updated Windows 10 or 11):  
	 ```
	 iex (curl.exe -s --doh-url https://1.1.1.1/dns-query https://get.activated.win | Out-String)
	 ```
	- **Script not launching? Use the below-listed Method 2.**

3. In the menu that appears, type the number corresponding to one of the **Green** options.

---

### Method 2 - Traditional (Windows Vista and later)

1.   Download the script:
      *   [**MAS_AIO.cmd**](https://dev.azure.com/massgrave/Microsoft-Activation-Scripts/_apis/git/repositories/Microsoft-Activation-Scripts/items?path=/MAS/All-In-One-Version-KL/MAS_AIO.cmd&download=true) (Direct script)
      *   [**MAS_AIO.zip**](https://dev.azure.com/massgrave/Microsoft-Activation-Scripts/_apis/git/repositories/Microsoft-Activation-Scripts/items?$format=zip) (If the direct script is blocked by your browser)
2.   Run the `MAS_AIO.cmd` file.
3.   In the menu that appears, type the number corresponding to one of the **Green** options.

---

> [!TIP]
> - Some ISPs/DNS providers block access to our domains. You can bypass this by enabling [DNS-over-HTTPS (DoH)](https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/encrypted-dns-browsers/) in your browser. 
> - **Having trouble**? Visit our [troubleshooting page](https://massgrave.dev/troubleshoot) or raise an issue on [GitHub](https://github.com/massgravel/Microsoft-Activation-Scripts/issues).

> [!NOTE]
>
> - The `irm` command in PowerShell downloads a script from a specified URL, and the `iex` command executes it.
> - Always double-check the URL before executing the command and verify the source is trustworthy when manually downloading files.
> - Be cautious of third parties spreading malware disguised as MAS by altering the URL in the PowerShell command.

---

<div align="center">
	
### Homepage - [https://massgrave.dev/](https://massgrave.dev/)
  
[![1.1]][1]
[![1.2]][2]
[![1.3]][3]
[![1.4]][4]
[![1.5]][5]
[![1.6]][6]
[![1.7]][7]

[1.1]: https://massgrave.dev/img/logo_discord.png (Chat with us without signup)
[1.2]: https://massgrave.dev/img/logo_reddit.png (Reddit)
[1.3]: https://massgrave.dev/img/logo_bluesky.png (Bluesky)
[1.4]: https://massgrave.dev/img/logo_x.png (Twitter)

[1.5]: https://massgrave.dev/img/logo_github.png (GitHub)
[1.6]: https://massgrave.dev/img/logo_azuredevops.png (AzureDevOps)
[1.7]: https://massgrave.dev/img/logo_gitea.png (Self-hosted Git)

[1]: https://discord.gg/j2yFsV5ZVC
[2]: https://www.reddit.com/r/MAS_Activator
[3]: https://bsky.app/profile/massgrave.dev
[4]: https://twitter.com/massgravel
[5]: https://github.com/massgravel/Microsoft-Activation-Scripts
[6]: https://dev.azure.com/massgrave/_git/Microsoft-Activation-Scripts
[7]: https://git.activated.win/Microsoft-Activation-Scripts

---

## Changes in This Fork

### [9] Turn Off Background Processes - CTT-style optimization

- One-click toggle in `MAS_AIO.cmd` that turns off background process bloat, inspired by Chris Titus Tech's Windows Utility:
  - **42** non-essential background services stopped and disabled
  - **22** privacy/performance registry tweaks (telemetry, Bing/Cortana search, Game DVR, activity history, Wi-Fi Sense, Delivery Optimization, ads and suggested content)
  - **15** telemetry scheduled tasks disabled (CEIP, Compatibility Appraiser, error-reporting queue, Maps, ...)
  - Switches to the **High Performance** power plan
- Everything is saved to `%ProgramData%\MAS_ProcessToggle\state.txt`; **[2] Turn Processes Back ON** restores every service start type, registry value, scheduled task, and your original power plan exactly.

### Change Windows Edition improvements

- New changeable targets: Windows 11/10 **LTSC** (`WNC`, `EnterpriseS`, `IoTEnterpriseS`) and **CloudEdition**, with clear warnings where an in-place change is unsupported or irreversible
- A pre-flight check refuses in-place changes Windows does not support (for example Pro to Home/LTSC) with a plain explanation instead of a cryptic DISM error code
- DISM/CBS failures are now surfaced instead of being silently swallowed

---

Latest Version: 3.12  
Release date: 04-Jul-2026
