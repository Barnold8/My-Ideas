
# Go Test Generator

Read a go file and make test file for it. If a test file already exists, check what tests exists and dont remake the tests, add to the tests


# Burner email server

An email server that can host any amount of burner emails. Add option for a burner email to forward its inbox to one other burner email address, like a parent burner email


# Windows chatbot

A chatbot in Python using NLTK that can assist elderly, less capable, or non-technically literate individuals with performing operations on Windows. Below are the features it can provide:

## System Maintenance
- **Clearing Temporary Files**: Assist in removing temporary files and freeing up disk space.
- **Managing Startup Applications**: Help disable unnecessary startup programs to improve boot time.
- **Updating Windows**: Guide users through checking for and installing Windows updates.
- **Setting Up System Restore Points**: Help create or manage system restore points.
- **Checking System Performance**: Provide an overview of CPU, RAM, and disk usage.
- **Installing/Uninstalling Software**: Simplify software installation or removal.
- **Scheduling Backups**: Help configure and schedule regular system or file backups.

## Accessibility Features
- **Enabling Accessibility Tools**: Enable tools like Narrator, Magnifier, or On-Screen Keyboard.
- **Adjusting Display Settings**: Help change resolution, text size, or enable high-contrast themes.
- **Configuring Speech Recognition**: Assist in setting up and using Windows' speech recognition.

## File Management
- **Searching for Files**: Help locate files or folders.
- **Organizing Files**: Assist in creating folders and moving/copying files.
- **Recovering Deleted Files**: Guide through checking the Recycle Bin or using Windows recovery tools.

## Networking
- **Connecting to Wi-Fi**: Help find and connect to Wi-Fi networks.
- **Troubleshooting Internet Issues**: Provide steps to resolve basic connectivity problems.
- **Sharing Files Over the Network**: Assist in setting up file sharing.

## Security
- **Running Virus Scans**: Integrate with Windows Defender or third-party antivirus tools.
- **Setting Up Passwords**: Help set or reset user account passwords.
- **Configuring Firewall Settings**: Simplify adjusting firewall rules or enabling/disabling the firewall.

## Customization
- **Changing Desktop Background**: Help choose and set wallpapers.
- **Organizing Taskbar and Start Menu**: Assist in pinning/removing apps from the taskbar or start menu.
- **Setting Up Shortcuts**: Guide users on creating desktop shortcuts.

## Miscellaneous
- **Explaining Error Messages**: Provide user-friendly explanations for common error codes.
- **Managing Printers**: Assist in adding, removing, or troubleshooting printers.
- **Configuring Time and Date Settings**: Help set the correct time zone or format.
- **Using Cortana or Search**: Offer instructions for making the most of Cortana or Windows search functionality.
- **Monitoring Battery Health (for laptops)**: Show battery wear levels and give tips for extending battery life.
- **Adjusting Volume and Sound Settings**: Guide users to troubleshoot or configure audio devices.

## Advanced Automation
- **Creating Batch Files**: Help automate repetitive tasks by creating simple batch scripts.
- **Setting Up Task Scheduler**: Guide through automating tasks like shutdowns or backups.

# Local CI/CD

## High-Level Workflow

### Repository Monitoring
- Use a tool or script to watch for changes in your repository (e.g., using Git hooks like `pre-push` or `post-commit`).

### Dockerized Language Environments
- Create Docker images tailored to each language or project. Each image would:
  - Install the language runtime (e.g., Python, Node.js, Go).
  - Set up project-specific dependencies (e.g., `requirements.txt`, `package.json`, `go.mod`).
- Use `docker-compose` for managing multiple containers if needed.

### Host-Container Communication
- Implement a mechanism to send the results back to the host:
  - Use a **shared volume** to write logs and a status file (e.g., `status.txt` containing `0` or `1`).
  - Use an **exit code** from the container process, which can be read by the host script.

### Test Execution
- Inside the container:
  - Run tests using the relevant test frameworks (e.g., `pytest`, `go test`, `jest`).
  - Write detailed logs to a shared volume accessible by the host.

### Host Program
- A lightweight script or program on the host (e.g., Python or Bash) could:
  - Trigger Docker container runs.
  - Monitor the status file or capture the container's exit code.
  - Collect logs and provide notifications or updates.

### Log Aggregation and Reporting
- Store logs in a structured format (e.g., JSON or plain text).
- Use a web interface or a CLI tool to view logs and test results.