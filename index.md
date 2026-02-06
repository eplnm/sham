## Quick recap

The meeting focused on setting up Python and its environment on Gabriel's Windows computer. Ukubona guided Gabriel through the installation process, which included installing WSL, Ubuntu, and various Python packages. They encountered some challenges due to Ukubona's lack of experience with Windows, but they successfully completed the setup. Gabriel learned how to create and run Python files using VS Code. They also discussed how to install additional packages and import them into Python scripts. The session ended with Ukubona promising to update the code to ensure Gabriel could see the output of simulations as images.
## Next steps

- [Gabriel: Save all terminal output and commands from the session in a Word document and send to Ukubona via email for instruction updates.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6def8-033f-11f1-9eb3-5a0e6771c2cf)
- [Ukubona: Update and improve the Windows onboarding instructions using the session notes provided by Gabriel.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6e468-033f-11f1-880b-5a0e6771c2cf)
- [Ukubona: Modify the code for session 1 so that the output image is saved and visible in VS Code, and share the updated code with Gabriel.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6e71c-033f-11f1-a696-5a0e6771c2cf)
- [Ukubona: Update Gabriel's session materials with clear instructions for creating and activating Python virtual environments, running Python files, and handling Windows-specific steps.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6e960-033f-11f1-b5c5-5a0e6771c2cf)
- [Ukubona: Notify Gabriel (via WhatsApp) when the updated notes and code are ready.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6eb72-033f-11f1-b146-5a0e6771c2cf)
- [Gabriel: Run the updated code for session 1 after receiving the modifications to check for correct image output.](https://us06tasks.zoom.us?meetingId=%2FiZNeFW4SFO6F6DpbAXlcQ%3D%3D&stepId=16c6ee19-033f-11f1-b3f9-5a0e6771c2cf)
## Summary

### Python WSL Setup Technical Session

Ukubona and Gabriel conducted a technical session focused on setting up a Python environment using WSL (Windows Subsystem for Linux). They reviewed and executed commands to install WSL, update Ubuntu, and configure the environment. Gabriel confirmed he had Ubuntu installed, and they successfully executed necessary commands to update the system. Ukubona emphasized that this setup process is a one-time task, unless Gabriel gets a new computer.
### Python Setup on Windows Guide

Ukubona and Gabriel worked through setting up a Python environment on Windows, encountering and resolving various configuration issues. They successfully installed Git for Windows, the WSL extension in VS Code, and created a Python virtual environment. Gabriel saved the detailed installation steps in a Word document and sent it to Ukubona's email for future reference. They also discussed how Python programs typically begin with importing necessary packages and that installing missing packages is straightforward. The session ended with Ukubona promising to improve the setup instructions for future users.
### Python Installation and Setup Guide

Ukubona guided Gabriel through the installation process of Python and its packages, explaining that while it's easier on a Mac due to its Linux-based operating system, they were working on a Windows computer. They successfully installed Python and several packages including pandas, and Ukubona assured Gabriel that once the initial setup was complete, he could run sessions independently using VS Code. Ukubona also mentioned that he would create additional practice materials for Gabriel beyond the initial 8 sessions, and Gabriel was instructed to create a Python file with a .py extension and copy the installed packages into it before running them using the Python command.
### VS Code Programming Basics

Ukubona and Gabriel discussed using VS Code for programming tasks, focusing on file creation and management. Ukubona guided Gabriel through creating a Python file, copying and pasting code, and using commands like MKDIR to create folders. They encountered an issue with running the Python script, which Ukubona noted needed further investigation.
### Python Environment Setup Challenges

Ukubona and Gabriel discussed setting up a Python environment on Gabriel's Windows machine. They encountered some challenges with file paths and command syntax due to differences between Windows and Linux/Mac systems. After troubleshooting, they successfully activated a virtual Python environment using WSL (Windows Subsystem for Linux) and were able to run a Python script. Ukubona acknowledged the complexity of the process and promised to create clearer, simplified steps for future reference.
### Python Virtual Environment Setup

The meeting focused on setting up Python and its virtual environment on Gabriel's Windows PC. Ukubona guided Gabriel through the process, explaining the importance of creating a virtual environment to manage Python's size and avoid slowing down the computer. They encountered some technical difficulties, including a slow installation process and connection issues, but successfully completed the setup. Ukubona promised to modify the code later to ensure Gabriel could see the output as a picture, and she planned to update Gabriel's sessions with instructions for future tasks.

# I
 
# Summary of Technical Setup Session Transcript

## Session Details
- **Participants**: Ukubona LLC (likely Abimereki D. Muzale, mentor/instructor) and Gabriel Ampaire (intern/student).
- **Purpose**: Troubleshooting and completing the setup of a Python development environment on Windows for running simulations and sessions (e.g., digital twin or AI-related tasks).
- **Platform**: Zoom video call with screen sharing; involves command-line operations in PowerShell, Ubuntu (via WSL), and VS Code.
- **Duration**: Approximately 1.5 hours, focused on resolving installation errors and configurations.
- **Key Challenges**: Windows-specific issues (e.g., backslashes vs. forward slashes, virtual environment activation, missing dependencies, slow installations due to internet or system).
- **Outcome**: Successful setup of Python, virtual environment, and running a sample script (s1.py), though output visualization needs code modification for Windows. Mentor promises updated notes and video.

## Essential Steps Captured
- **Initial Setup (WSL and Ubuntu)**:
  - Install WSL via PowerShell: `wsl --install` (or `winget install --id=9P9TQF7MRMRQ` if not found).
  - Run Ubuntu, set username/password.
  - Update packages: `sudo apt update && sudo apt upgrade -y`.

- **Install Dependencies for Python**:
  - Install build essentials: `sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev`.
  - Resolve errors (e.g., missing C compiler) by installing additional tools.

- **Pyenv and Virtual Environment**:
  - Install pyenv: `curl https://pyenv.run | bash`.
  - Add pyenv to shell config: Edit `~/.bashrc` with `export PATH="$HOME/.pyenv/bin:$PATH"`, `eval "$(pyenv init --path)"`, `eval "$(pyenv virtualenv-init -)"`.
  - Source config: `source ~/.bashrc`.
  - Install Python version: `pyenv install 3.12.3` (or similar).
  - Create virtual env: `pyenv virtualenv 3.12.3 venv` (or `python3 -m venv venv`).
  - Activate: `source venv/bin/activate` (use forward slashes for Linux/WSL).

- **Install Python Packages**:
  - In activated env: `pip install numpy matplotlib pandas scipy streamlit` (common for data, plots, etc.).
  - Handle slow installs or errors (e.g., check internet, retry).

- **VS Code Integration**:
  - Install WSL extension in VS Code.
  - Open VS Code in WSL: `code .` (creates/opns .py files).
  - Create file: `code s1.py`, paste code, save.
  - Run script: `python s1.py` (or `python3 s1.py` if needed).

- **Troubleshooting Highlights**:
  - Switch to WSL mode: `wsl` in PowerShell to enter Linux shell (forward slashes).
  - Path issues: Use `pwd` to check current directory; `cd /path/to/dir` to navigate.
  - Errors fixed via AI (Gemini): Pasted error messages for solutions (e.g., missing configs, activations).
  - Windows vs. Linux/Mac: Windows requires extra steps (WSL); Mac/Linux are simpler.

- **Final Notes**:
  - Session workflow: Start with `wsl`, create/activate venv, install packages if needed, run scripts.
  - No permanent space usage (virtual envs are temporary).
  - Mentor to provide updated code for visualization (e.g., save plots as files) and refined Windows instructions.
  - Future: Independent running of 8+ sessions; contact via WhatsApp/email for issues.

This captures the core process for replicating the setup, emphasizing Windows-specific adaptations.
 
# II
### Mac vs. Windows Setup Comparison for Python Development

Based on the context of setting up a Python development environment (as discussed in technical sessions like the one in your transcript), I'll compare Mac (macOS) and Windows setups. This focuses on ease of installation, compatibility, performance, and common use cases for tasks like virtual environments, VS Code integration, and running scripts/simulations. Mac is generally simpler due to its Unix-based foundation, while Windows requires extra steps (e.g., WSL for Linux-like functionality). Insights draw from developer experiences, including Reddit discussions, Quora, YouTube analyses, and Medium articles.

#### Key Advantages and Disadvantages
- **Mac (macOS)**: Built on Unix (similar to Linux), so native support for many tools. Ideal for beginners or those avoiding extra configuration.
- **Windows**: More hardware options and affordability, but setup involves workarounds for Unix-dependent tools like Python.

| Aspect                  | Mac (macOS)                                      | Windows                                          |
|-------------------------|--------------------------------------------------|--------------------------------------------------|
| **Ease of Initial Setup** | Very straightforward. No need for WSL—install Python via Homebrew (`brew install python`) or directly. Virtual environments (venv) work natively. Takes ~10-15 minutes. | Requires Windows Subsystem for Linux (WSL) for Unix compatibility. Steps include enabling WSL, installing Ubuntu, updating packages (`sudo apt update`), and configuring paths. Can take 30-90 minutes with troubleshooting (e.g., path errors, backslashes vs. forward slashes). |
| **Python Installation** | Native support; use `python3` out of the box. Tools like pyenv for version management install easily. | Use WSL for Linux-like install (`pyenv install`). Native Windows Python works but may have issues with Unix scripts. Often needs `python3` alias. |
| **Virtual Environments** | Simple: `python3 -m venv venv` and `source venv/bin/activate`. No platform-specific hacks. | In WSL: Same as Mac, but activate with `source venv/bin/activate`. PowerShell may need `. venv\Scripts\Activate.ps1`. Path issues common (e.g., backslashes). |
| **VS Code Integration** | Seamless: Install VS Code, add extensions (e.g., Python, WSL if needed but rarely). Native terminal supports Bash/Zsh. | Install WSL extension first. Run `code .` in WSL to open projects. Switching between Windows/PowerShell and WSL terminals can be clunky. |
| **Performance** | Excellent for everyday dev; M-series chips (e.g., M1/M2) optimize for AI/ML (e.g., faster TensorFlow/PyTorch). Battery life superior. | Good with high-end hardware (e.g., RTX GPUs for ML), but WSL overhead can slow I/O. Better for gaming/dev hybrids. |
| **Common Tools/Packages** | Native compatibility with Git, Node.js, Docker. Fewer errors for web dev (e.g., Django, Rails). | WSL handles most (e.g., `pip install numpy matplotlib`), but occasional Windows-specific bugs (e.g., file paths, compilers). |
| **Pros** | - Unix-like (no WSL needed).<br>- Better for iOS/macOS dev integration.<br>- Smoother for scripting/AI (e.g., native Metal for ML acceleration). | - Cheaper hardware variety.<br>- Native .NET/C# support.<br>- WSL2 bridges gaps effectively for Linux tools. |
| **Cons** | - Expensive hardware.<br>- Less customizable (e.g., no easy GPU upgrades). | - More setup friction (e.g., errors like "source not recognized").<br>- Potential for cross-platform bugs. |
| **Best For** | Python/web/ML devs valuing simplicity (e.g., no extra layers like WSL). | Budget-conscious users or those in Microsoft ecosystems (.NET, Azure). Use if you need powerful GPUs without Apple premiums. |

#### Recommendations
- **Choose Mac if**: You're new to setup, prioritize speed/simplicity, or work in AI/ML (Apple Silicon excels). From your transcript, Mac avoids the WSL pains you experienced on Windows.
- **Choose Windows if**: You want flexibility/affordability, or integrate with enterprise tools. WSL makes it viable for Python, but expect initial hurdles.
- **Hybrid Tip**: On Windows, always start sessions with `wsl`, create/activate venv, then run scripts. For advanced users, dual-boot Linux (e.g., Ubuntu) eliminates WSL entirely.

If you need a deeper dive (e.g., specific to kidney simulation code or tools like Streamlit), let me know!

## III
Coming Soon..