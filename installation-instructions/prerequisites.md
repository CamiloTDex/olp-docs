# Prerequisites



### Prerequisites for your personal workstation (If you are installing OLP node into a remote/virtual machine)



To install OLP Node onto a cloud-based Virtual Machine or a remote server, you can use any PC/Mac/Linux or even Android/iOS as long as it has Command Line / Terminal app which allows controlling such Virtual Machine over SSH protocol (or any other way of remotely controlling such Virtual Machine or server where you want OLP node to be hosted)



### Prerequisites for the machine that will run the node

We recommend you create a VM with the following attributes: Memory size: Set to 6 GB (recommended) Create a virtual hard disk with at least 10 GB (20 GB recommended) Virtual hard disk file type: VDI (if you need to share it with other apps, use VHD) (Optional) You can create a shared directory to copy block files or genesis files from the host computer to the VM

* OS Requirements for the node:
  * Linux on x86\_64 architecture
  * macOS on an Intel processor (M1 processor not supported yet)
  * Windows 64-bit edition, with: Windows Subsystem for Linux 2 Docker desktop configured to use the WSL2-based engine
* Required Software:
  * Docker and Docker Compose \*(Allows running the OLP node as a service container or virtualized environment)\*
    * Ubuntu: [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/)
    * MacOSX: [https://docs.docker.com/desktop/install/mac-install/](https://docs.docker.com/desktop/install/mac-install/)
    * Windows: [https://docs.docker.com/desktop/install/windows-install/](https://docs.docker.com/desktop/install/windows-install/)
  * Node.js Version 16 or higher \*(Javascript runtime environment used for the backend of the OLP node)\*
    * Download: [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
  * (macOS Only) - XCode development tools \*(Required for using git)\*
    * Download: [https://developer.apple.com/xcode/resources/](https://developer.apple.com/xcode/resources/)
  * &#x20;Git (Required to download the sources):
    * [https://git-scm.com/downloads](https://git-scm.com/downloads)&#x20;
  * unzip command line tool (Required to unzip the sources):
    * By default installed in MacOSX
    * In Linux check if installed using \*unzip -h\*, if not install by using \`sudo apt-get install zip unzip\`
* Required Open Ports in the node machine:
  * 7577 - Installation Wizard Port
  * 9560 - HTTP Port (This port can be changed in wizard)
  * 9561 - P2P Port (This port be changed in wizard)
