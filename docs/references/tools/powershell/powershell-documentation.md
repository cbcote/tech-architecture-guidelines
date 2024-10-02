# Powershell Documentation

## 1. Introduction to PowerShell
### What is PowerShell?
- **PowerShell** is a task automation and configuration management framework from Microsoft.
- It includes a command-line shell and a scripting language built on .NET.
- PowerShell is cross-platform and can run on Windows, Linux, and macOS.

### Why Use PowerShell?
- Combines the interactive shell and scripting capabilities, allowing administrators and developers to automate tasks.
- Works with both standard commands and .NET objects, providing powerful capabilities for managing systems.
- Cross-platform compatibility allows PowerShell to be used in different environments.

## 2. PowerShell Basics
### Shell Basics
- **Shell**: A command-line interface that allows users to interact with the operating system.
- PowerShell interprets commands, returns output, and interacts with the file system.
- **Cmdlets**: Specialized commands in PowerShell, such as `Get-Command`, `Get-Help`, and `Set-ExecutionPolicy`.

### How PowerShell Works
- PowerShell commands are **cmdlets** with a verb-noun naming convention, such as `Get-Process` or `Set-Service`.
- Commands are case-insensitive and can handle input and output as objects.
- PowerShell is designed for automation tasks such as system administration, configuration, and scripting.

## 3. Key Features of PowerShell
### Cmdlets and Pipelines
- PowerShell cmdlets output objects, making it easier to manipulate data and perform tasks.
- **Pipelines**: PowerShell can pass objects (not just text) between commands using pipelines (`|`).
  
### PowerShell Scripting
- PowerShell allows users to write scripts to automate repetitive tasks.
- **Script files**: PowerShell scripts use `.ps1` file extensions and can include variables, loops, and conditionals.
- **Shebang support**: PowerShell Core supports shebang (`#!/usr/bin/env pwsh`) for cross-platform script compatibility.

### Modules
- PowerShell modules are packages of cmdlets that extend functionality.
- Examples: `ActiveDirectory`, `AzureRM`, `ExchangeOnlineManagement`.
- Modules can be installed and imported into PowerShell sessions using `Install-Module` and `Import-Module`.

### Object-Oriented Nature
- PowerShell commands return **objects** instead of plain text.
- Objects can be manipulated in many ways using properties and methods.
- Example: Use `Get-Process | Sort-Object CPU` to sort running processes by CPU usage.

## 4. PowerShell Scripting Basics
### Variables and Data Types
- Variables in PowerShell are declared using `$`, e.g., `$variable = "Hello World"`.
- Supports various data types like strings, integers, arrays, and hashtables.
  
### Control Structures
- **If-Else**: Conditional statements for decision making.
- **ForEach-Object**: Loop through objects in the pipeline.
- **Switch**: Used for handling multiple conditions.

### Functions
- PowerShell functions are reusable blocks of code that can accept parameters and return values.
- Example:
  ```powershell
  function Get-Square {
      param([int]$number)
      return $number * $number
  }
