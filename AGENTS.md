# AGENTS

## Project Description

This project is a workspace for using AI to assist with everyday work.

## Workspace Organization

Use `.process/` only for intermediate artifacts, temporary working files, and files whose final destination has not yet been determined.

When a task involves creating or processing files, create a directory in the project root named with the current date in `YYYYMMDD` format. Store the task-related files in that dated directory, and place all processing results in its `result/` subdirectory.

The dated directory for the current date is the current work area. By default, only read task files within the current work area. Do not inspect or read files in work areas from previous dates unless the user gives an explicit instruction to read them. Project-level instruction files may be read when needed to operate within this workspace.

## Operation Scope

Perform all operations at the project level by default. Do not create, install, configure, modify, or store anything globally or at the user level unless the user explicitly instructs you to perform that specific operation globally.

## Agent Memory

Store all persistent agent memory for this workspace inside the current project directory. Do not create or update agent memory in global, user-level, or other locations outside the project, even if those locations are scoped or named for this project.

## Python Environment

When Python is needed, only use the `small_tools` Conda environment. Do not use the system Python interpreter, another Conda environment, or any other Python environment.

Python packages required for a task may be installed in the `small_tools` environment. Do not install them in the system Python environment or any other global environment.

## Node.js Environment

When Node.js is needed, use the locally installed Node.js 24 environment rather than a runtime bundled with an AI tool.

## Other Tool and Package Installation

Except for Python packages installed in the `small_tools` environment, do not use system commands to download or install tools, packages, or dependencies. When another installation is required, provide the exact command and wait for the user to run it manually.

## Deletion Operations

Do not execute any deletion operation, including deleting files, directories, data, packages, or resources. When deletion is required, explain why, provide the exact command or steps, and wait for the user to perform it manually.

## Response Formatting

Use bullet points sparingly in responses. Prefer tables when presenting structured information that benefits from comparison or categorization.

Do not use emojis in responses.
