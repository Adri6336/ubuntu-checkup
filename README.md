# ubuntu-checkup
Ubuntu-checkup is a comprehensive Linux system repair and reporting tool designed to maintain the health of Ubuntu-derived systems. By automating routine maintenance tasks and generating detailed system health reports, it serves as a one-stop solution for keeping your system optimized and secure.

# Features
- **System Updates**: Automates the process of updating and upgrading installed packages to ensure your system is up-to-date.
- **Disk Usage Monitoring**: Provides detailed insights into disk space utilization across all mounted filesystems.
- **Memory and CPU Analysis**: Reports on memory usage and CPU load to help identify performance bottlenecks.
- **SMART Disk Status**: Checks the health of your storage devices using SMART diagnostics.
- **System Logs Review**: Analyzes recent system logs for errors, failures, and critical events, providing explanations for common issues.
- **Package Integrity Checks**: Uses debsums to verify the integrity of installed packages and attempts repairs for corrupted ones.
- **HTML Reporting**: Compiles all findings into a structured and easy-to-read HTML report for quick reference.
- **Customizable Options**: Offers various flags to skip specific checks, specify log/report file locations, and more.

![Log](https://github.com/user-attachments/assets/b9606e01-ef35-4fb1-94d4-2202b95bad32)

# Installation

1: Clone the Repository

    git clone https://github.com/Adri6336/ubuntu-checkup.git
    cd ubuntu-checkup
   
2: Make the Script Executable


    chmod +x checkup

3: Move to a Directory in Your PATH

    sudo mv checkup /usr/local/bin/
   
# Usage
Run the checkup script with root privileges to perform a full system check and generate a health report.

    sudo checkup
    
# Options
-n, --no-update
Skip the system update and upgrade steps.

-s, --skip-smart
Skip SMART disk checks.

-d, --no-debsums
Skip debsums package integrity checks.

-l, --log-file FILE
Specify an alternate log file path. Default: /var/log/system_maintenance.log

-r, --report-file FILE
Specify an alternate report file path. Default: $USER_HOME/system_health_report_<timestamp>.html

-h, --help
Show the help message and exit.

# Examples

Run a full system check and generate a report:

    sudo checkup
    
Run checkup but skip SMART checks and system updates:

    sudo checkup --skip-smart --no-update

# Dependencies
The script relies on several utilities to perform its tasks. These include:

1. apt-get
2. smartctl (from smartmontools)
3. debsums
4. Standard Unix utilities (grep, awk, sed, etc.)

The script will attempt to install any missing dependencies automatically.


