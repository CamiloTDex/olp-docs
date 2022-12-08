# Prerequisites to Run a Node

We recommend you create a VM with the following attributes:
Memory size: Set to 6 GB (recommended)
Create a virtual hard disk with at least 10 GB (20 GB recommended)
Virtual hard disk file type: VDI (if you need to share it with other apps, use VHD)
(Optional) You can create a shared directory to copy block files or genesis files from the host computer to the VM

* OS Requirements:
  * Linux on x86_64 architecture
  * macOS on an Intel processor (M1 processor not supported yet)
  * Windows 64-bit edition, with:
    Windows Subsystem for Linux 2
    Docker desktop configured to use the WSL2-based engine
* Required Software:
  * Docker and Docker Compose (allows running the OLP node as a service container or virtualized environment)
  * Node.js Version 18 or higher (Javascript runtime environment used for the backend of the OLP node)
  * MongoDB 4.0 or higher: database used by the OLP Node
  * Nginx: web server for the OLP Node
  * cURL command line: tool to transfer data using HTTP by the P2P layer of the OLP node
  * MetaMask
* Required Open Ports:
  * 7577 - Installation Wizard Port
  * 9560 - HTTP Port (Configurable in wizard)
  * 9561 - P2P Port (Configurable in wizard)

