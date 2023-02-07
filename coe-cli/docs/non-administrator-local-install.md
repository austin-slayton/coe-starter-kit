---
title: "Center of Excellence (CoE) Command Line Interface (CLI) non administrator installation"
description: "Install instructions for the Center of Excellence Command-Line interface using non administrator rights"
keywords: 
author: Grant-Archibald-MS
ms.author: grarchib
manager: yasinm
ms.custom: ""
ms.date: 3/15/2022
ms.topic: "article"
ms.reviewer: jimholtz
search.audienceType: 
  - admin
search.app: 
  - PowerApps
  - Powerplatform
---

# Non Administrator Center of Excellence (CoE) Command Line Interface (CLI) installation

To install the CoE CLI as a non-administrator you leverage use the following components:

- Follow [Miniconda Install](#miniconda-install) instructions for your operating system.

- [Local NodeJs](#local-nodejs) with non-admin install.

- Install [Standalone Power Platform CLI](/powerapps/developer/data-platform/powerapps-cli#standalone-power-platform-cli).

## Miniconda install

Miniconda is a free minimal installer for conda. It is a small, bootstrap version of Anaconda that includes only conda, Python, the packages they depend on, and a small number of other useful packages.

1. Visit [Minoconda](https://docs.conda.io/en/latest/miniconda.html) to download.

1. Install Miniconda for your operating system.

## Local NodeJs

To install NodeJs using non-administrator install by following the steps:

1. Go to [NodeJs Download](https://nodejs.org/en/download/).

1. Download the Windows binary for your operating system type.

1. Open the downloaded the zip file.

1. In Windows Explorer open **%USERPROFILE%**.

1. Create a folder named *nodejs*.

1. Copy all files from zip file into **nodejs** folder.

## Install components

### Microsoft Windows

To install components using Microsoft Windows:

1. Open %USERPROFILE%\dev.bat with Notepad and make the following edit:

  ```text
  SET PATH=%PATH%;%USERPROFILE%/nodejs
  %windir%\System32\cmd.exe "/K" %USERPROFILE%\miniconda3\Scripts\activate.bat %USERPROFILE%\miniconda3
  ```

1. Open **dev.bat** file created earlier.

1. Install the Azure CLI.

  ```cmd
  pip install azure-cli
  ```

1. Verify all prerequisites are now all installed.

  ```cmd
  az --version
  node --version
  pac
  ```

1. Download the zip file or clone the repository [coe-starter-kit](https://github.com/microsoft/coe-starter-kit).

1. Go to the unzipped or cloned repository.

   ```cmd
   cd coe-starter-kit
   ```

1. Go to the **coe-cli** folder.

   ```cmd
   cd coe-cli
   ```

1. Install application dependencies.

   ```cmd
   npm install
   ```

1. Build the application.

   ```cmd
   npm run build
   ```

1. Link to the CoE CLI application.

   ```cmd
   npm link
   ```

1. Ensure the CoE CLI is installed.

  ```cmd
  coe help    
  ```
