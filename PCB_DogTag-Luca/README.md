# PCB_DogTag

## Description

This repository contains Altium PCB files for UBC Thunderbots' introductory project, the Dog Tag. Anyone who wishes to push changes to this project must get permission from the current Electrical Team Lead.

## Getting Started

### Required software

1. git
2. Altium Designer

### Instructions

1. Either create a new working branch or select an existing branch other than `master` or `main`.
2. **Clone** (`git clone`) your working branch of the repository to your PC (i.e. `C:/Documents/thunderbots/PCB_DogTag`).
3. In Altium Designer, navigate to *Preferences -> Data Management -> Version Control* and ensure **SVN - Subversion** is enabled and **Version 1.9** is selected.
4. In Altium Designer, navigate to *Preferences -> Data Management -> Design Repositories*.
5. Within *Design Repositories* click on on *Connect To* -> **SVN**.
6. In the dialogue box that comes up, fill in the following information:

Field|Selection/Input
---|---
Name|PCB_Power
Default Checkout Path|location of local repository (i.e. `C:/Documents/thunderbots/PCB_DogTag`)
Method|https
Server|github.com
Server Port|Default
Repository Subfolder|/UBC-Thunderbots/PCB_Power
User Name|*your github login username*
Password|*your github login password*

7. Click **Test**.

After your repository is connected, you can add or remove files like a regular Altium Project folder and then commit and push your changes to the remote repository.

[Reference](https://forum.live.altium.com/#posts/235981/718003)

## Repository Structure

At the highest level, there should be the most up to date board revisions, (e.g.
`power-v1.0/`), `archive/`, and `Altium_Libraries/`. Any previous versions should be placed in `archive/`. Every board revision directory should abide by the following structure:

```
<name-v#>/
├── doc/
│   ├── <name>.pdf
│   └── <name>.xslx or <name>.csv
├── pcb/
│   ├── guidelines/
│   ├── <name>.PrjPCB
│   ├── <name>.SchDoc
│   └── <name>.PcbDoc
└── sim/
```

### doc/

For documentation and relevant non-simulation and layout files. This includes PDFs of the design and bills of materials (`*.xlsx` or `.csv` format).

### pcb/

For any PCB design software files related to the schematic capture and PCB layout of board. This includes schematic and PCB layout guidelines (`guidelines/`).

### sim/

For any simulation files related to the PCB design here.
