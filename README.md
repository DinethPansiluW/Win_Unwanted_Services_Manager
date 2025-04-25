# Windows Services Manager Script

This script is a tool for managing Windows services, providing an interactive menu for users to control, configure, and automate the state of essential services. It simplifies the process of managing services for system administrators and power users.

## Features

- **Manage Services**: Start, stop, and configure the state of essential Windows services.
- **Backup and Restore**: Backup live service status and restore from a backup.
- **Bulk Service Control**: Enable, disable, or modify all services at once.

## Installation

1. Download or clone the repository to your local machine.
2. Ensure you have the necessary administrative privileges to run scripts that interact with Windows services.
3. Execute the script using a PowerShell terminal or Command Prompt with administrative rights.

## Usage

Run the script to launch the main menu, where you'll have several options to manage the services on your system.

### Menu: 
```
=============== MAIN MENU ===============
1. Print Spooler-------------- [ Automatic | Running ]
2. SysMain-------------------- [ Disabled | Stopped ]
3. Windows Update------------- [ Disabled | Stopped ]
4. Windows Time--------------- [ Automatic | Stopped ]
5. Launch Hyper-V------------ [  | Stopped ]
...

- Backup Live Status                ( b  )
- Restore from Backup               ( r  )
- Restore to Script 1st Launch      ( r1 )

- Enable All Services               ( ea )
- Disable All Services              ( da )
- Manual | Running All              ( mr )
- Manual | Stopped All              ( ms )
- Run All                           ( ra )
- Stop All                          ( sa )

- Exit                              ( e  )
========================================
Select :
```
### Main Menu Commands:

- **1 to last service number**: Select a service by its number (e.g., `1` for Print Spooler, `2` for SysMain) to view detailed information about that service. Each service will have options for enabling, disabling, setting to manual, stopping, and returning to the main menu.
- **Backup Live Status (`b`)**: Backs up the current state of all services.
- **Restore from Backup (`r`)**: Restores services from the most recent backup.
- **Restore to Script 1st Launch (`r1`)**: Restores services to their original state when the script was first launched.
- **Enable All Services (`ea`)**: Enables all services to start automatically.
- **Disable All Services (`da`)**: Disables all services to prevent them from starting.
- **Manual | Running All (`mr`)**: Sets all services to run manually and ensures they are started.
- **Manual | Stopped All (`ms`)**: Sets all services to manual start and ensures they are stopped.
- **Run All (`ra`)**: Starts all services.
- **Stop All (`sa`)**: Stops all running services.

When you choose a numbered service (e.g., selecting **1** for the Print Spooler), you'll be taken to the following service-specific menu:

### Example: Print Spooler Service Menu
```
===== Print Spooler Service Menu =====
Service: Spooler
Description: Manages print jobs; disabling stops all printing.
Startup Type: Automatic
Status: Running
=====================================
1. Enable (Automatic)
2. Disable
3. Set to Manual
4. Stop Service
5. Return to Main Menu

Choose (1-5):
```
### Service Menu Commands:

- **Enable (Automatic) (`1`)**: Sets the service to "Automatic" startup type and ensures the service is running.
- **Disable (`2`)**: Disables the service, preventing it from starting automatically.
- **Set to Manual (`3`)**: Sets the service to "Manual" startup type.
- **Start/Stop Service (`4`)**: Start/Stops the service.
- **Return to Main Menu (`5`)**: Returns to the main menu where you can choose other services or commands.


## Requirements

- Windows operating system (Windows 7 or higher recommended)
- PowerShell or Command Prompt with administrative privileges

## Contributing

If you would like to contribute to this project, feel free to fork the repository, make your changes, and submit a pull request. Please ensure that your contributions are aligned with the original purpose of the script.

## License

This script is licensed under the MIT License.


