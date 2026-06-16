# eXpOS (Experimental Operating System) Implementation

An implementation of **eXpOS** (Experimental Operating System), a multiprogramming operating system designed for the XSM (Experimental String Machine) architecture. This project involves building the core components of an operating system kernel, including memory management, process scheduling, interrupt handling, and system call interfaces from scratch.

Following the official [eXpOS NITC Roadmap](https://exposnitc.github.io/Roadmap.html).

---

## 📁 Repository Structure

```text
myexpos/
├── spl/                  # SPL Compiler and associated tools
├── expl/                 # ExpL Compiler and library files
├── xsm/                  # XSM Simulator execution environment
└── workdir/              # Active development directory
    ├── stage 1/          # Simulator familiarization
    ├── stage 2/          # Understanding the file system
    ├── stage 3/          # Bootstrap loader
    ├── stage 4/          # Learning the SPL language
    ├── stage 5/          # XSM Debugging
    ├── stage 6/          # Running a user program
    ├── stage 7/          # ABI and XEXE Format
    ├── stage 8/          # Handling Timer Interrupt
    ├── stage 9/          # Handling kernel stack
    ├── stage 10/         # Console output
    ├── stage 11/         # Introduction to ExpL
    └── stage 12/         # Introduction to multiprogramming

Stage,Milestone,Description,Status
Stage 1,XSM Architecture,Introduction to the XSM simulator instruction set.,Completed
Stage 2,File System Basics,Understanding the structure of the XFS file system.,Completed
Stage 3,Bootstrap Loader,Writing a basic boot loader code to load blocks from disk to memory.,Completed
Stage 4,SPL Language,Familiarization with System Programmer's Language (SPL).,Completed
Stage 5,XSM Debugging,Utilizing the XSM debugger to trace execution steps.,Completed
Stage 6,Running a User Program,Loading and executing a basic single-user program block.,Completed
Stage 7,ABI & XEXE Format,Implementing the Application Binary Interface and understanding executable headers.,Completed
Stage 8,Timer Interrupt,Setting up hardware timer interrupts and handling switching mechanics.,Completed
Stage 9,Kernel Stack Management,Managing separate user and kernel mode stacks safely during switches.,Completed
Stage 10,Console Output,Implementing interrupt-driven or polling-based console output.,Completed
Stage 11,Experimental Language,Introduction to high-level system applications using ExpL.,Completed
Stage 12,Multiprogramming,Initial execution setup for concurrent running processes.,Completed

🛠️ Tools & Technologies Used
Design Framework: eXpOS Specification Architecture

System Language: SPL (System Programmer's Language)

Application Language: ExpL (Experimental Language)

Target Hardware: XSM (Experimental String Machine) Simulator

Version Control: Git & GitHub

⚙️ How to Compile and Run (General Workflow)

Bash
   ./spl path_to_spl_file.spl
Compile the User Program (ExpL):

Bash
   ./expl path_to_expl_file.expl
Load files onto the Virtual Disk:
Open the XFS-Interface tool to format and load the compiled .xsm binary code blocks into appropriate OS slots.

Execute on Simulator:
Run the machine emulator environment:

Bash
   ./xsm
