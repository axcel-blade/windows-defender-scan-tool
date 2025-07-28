# Windows Defender Scan Tool

A user-friendly batch script that provides a menu-driven interface for Windows Defender's built-in scanning capabilities. This tool simplifies access to various scan types without needing to remember complex command-line parameters.

## Features

- **Interactive Menu Interface** - Easy-to-use command-line menu system
- **Multiple Scan Types** - Quick, Full, Custom, Offline, and Boot Sector scans
- **Safety Confirmations** - Prompts for potentially disruptive operations
- **Error Handling** - Validates paths and provides helpful error messages
- **Administrator Detection** - Works best when run with elevated privileges

## Scan Types

### 1. Quick Scan
- Scans the most common locations where malware is typically found
- Fast execution (usually completes in minutes)
- Ideal for routine security checks

### 2. Full Scan
- Comprehensive scan of the entire system
- Scans all files and running programs
- Can take several hours to complete
- Includes confirmation prompt due to time requirement

### 3. Custom Scan
- Allows you to specify a particular folder or drive path
- Perfect for scanning suspicious directories or external drives
- Validates path existence before scanning

### 4. Microsoft Defender Offline Scan
- Restarts the computer and runs a pre-boot scan
- Effective against rootkits and persistent malware
- **Warning:** Will restart your computer automatically
- Includes multiple confirmation prompts

### 5. Boot Sector Scan
- Scans boot sectors for rootkits and boot-level malware
- Targets areas that are difficult to scan while Windows is running
- Quick execution compared to full system scans

## Requirements

- Windows 10/11 with Windows Defender enabled
- Administrator privileges (recommended for full functionality)
- Windows Defender command-line tool (MpCmdRun.exe) must be available

## Installation

1. Download the `DefenderScan.bat` file
2. Save it to a convenient location on your computer
3. Right-click the file and select "Run as administrator"

## Usage

1. **Launch the Script**
   ```cmd
   Right-click DefenderScan.bat → "Run as administrator"
   ```

2. **Select Scan Type**
   - Choose from options 1-6 using the number keys
   - Follow on-screen prompts for confirmation when required

3. **Monitor Progress**
   - The script will display scan progress and results
   - Press any key to return to the main menu after scan completion

## Example Usage

```
===============================================
         Windows Defender Scan Tool
===============================================

Please select the type of scan you want to run:

[1] Quick Scan
[2] Full Scan
[3] Custom Scan (specify folder)
[4] Microsoft Defender Offline Scan
[5] Boot Sector Scan
[6] Exit

Enter your choice (1-6): 1
```

## Important Notes

⚠️ **Administrator Rights Required** - Run the script as administrator for full functionality

⚠️ **Offline Scan Warning** - The offline scan option will restart your computer. Save all work before proceeding.

⚠️ **Full Scan Duration** - Full scans can take several hours depending on system size and file count.

## Troubleshooting

### Common Issues

**"Windows Defender command line tool not found"**
- Ensure Windows Defender is enabled in Windows Security settings
- Verify that Windows Defender is not disabled by group policy
- Check if a third-party antivirus has replaced Windows Defender

**"Access Denied" Errors**
- Run the script as administrator
- Ensure Windows Defender Real-time Protection is enabled

**Custom Scan Path Not Found**
- Verify the path exists and is accessible
- Use full paths (e.g., `C:\Users\YourName\Documents`)
- Avoid using mapped network drives for reliability

## Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

### Suggested Improvements
- Add logging functionality
- Include scan scheduling options
- Add support for exclusion lists
- Implement scan result parsing and reporting

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This tool is provided as-is for educational and administrative purposes. Always ensure you have proper backups before running system scans. The authors are not responsible for any system issues that may arise from the use of this tool.

## Support

If you encounter issues or have questions:
1. Check the troubleshooting section above
2. Review Windows Defender documentation
3. Submit an issue on this repository

---

**Version:** 1.0  
**Last Updated:** July 2025  
**Compatibility:** Windows 10, Windows 11