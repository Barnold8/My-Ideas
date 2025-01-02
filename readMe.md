oh
# Go Test Generator - DONE

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


# Minecraft server - single player world sync

A program to allow small servers (that with friends usually) to sync up a world file/save so friends can play offline after the server goes offline for the day.

Its going to be hard to sync up changes, but it wont be impossible


# Android spelling assistant for kids

An app that scans spelling homework and generates a fun test to do for the learning child, no paper or pen required! 

New idea for this idea, make a game in godot since it can be compiled for IOS and Android and can gameify the learning process making it fun to learn. Can add features like outfits for a character that can be purchased in game with earned currency. Could have multiple learning criteria like

- Spelling
- Maths
- Science
- Geography


# Godot horror game **dishevelled** 

## rough idea 

intro is a slow drive into a forest

searching woods for something 

creepy woman can sink into floor and pursue the player 

maybe look like ps1 with shaders 

voice detection for horror, maybe creepy woman can follow the person based on noise 

cabin in the woods 

searching for answers 


## story

### backstory 

you are a person who decides through their work if people can get the treatment for easily curable ills. however you are evil to say the least and allowed a lot of these people to not get the care they needed to put more money in your pocket and they subsequently passed. the company you work for goes bust leading you on the verge of bankruptcy.and by a twist of messed up fate your pregnant wife needed easily accessible healthcare and she was denied like the many people you denied leading to her and the babies demise. 

### game start 

{opening cutscene}

view from inside the car 

driving down the motorway late at night, no other cars in sight, the colour of the scene is more yellow than anything because of the lights on the motorway being the only source of light. you hear nothing but the car driving down the road and then the player turns on the radio. the radio mentions something along the lines of a once respected man now vilified being killed in broad daylight

camera pans out of the car to show the car turning off of the motorway. as this pan is happening, the title sequence happens 


{you're now in a forest with your car blocking the exit and the car lights are illuminatimg the path into the forest}

the gameplay is a mix of exploration and horror. there will be notes around giving hints to the backstory previously mentioned. 

throughout the game you will come into contact with the souls of the dead you caused. each soil is a vengeful spirit with characteristics that depict how they died. 


{endgame) 

you come into contact with a door that opens up to a street on broad daylight. this transitions to a cutscene 

{ending cinematic}

you walk through the door, blasted with daylight in the eyes, you turn around to see a gun barrel in your face, the trigger is pulled and a flash of light hits your eyes, this then trsnsitions into seeing your body on the floor from a top down view, the camera slowly moves up into the sky showing the title again, while the camera is panning up, the same radio broadcast you heard at the start of the game is being heard again 
