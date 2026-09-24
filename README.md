# Global
## Universal Keyboard Layout Translator for Windows

### Tagline

> Type in the wrong language? Recover instantly.

---

# Overview

Global is a lightweight Windows application that allows users to instantly convert text typed using the wrong keyboard layout.

The application supports keyboard layouts from multiple countries and enables real-time or on-demand conversion between layouts such as:

```text
English ↔ Thai
English ↔ Russian
English ↔ Korean
English ↔ Japanese
English ↔ Chinese
English ↔ Arabic
English ↔ Hebrew
English ↔ Greek
English ↔ Ukrainian
```

Global runs in the background, integrates with Windows, and works across virtually all applications including browsers, Office, IDEs, chat tools, and desktop applications.

---

# Problem Statement

Millions of users work in multilingual environments and frequently type with the wrong keyboard layout actively selected.

Examples include:

### English Intended, Thai Layout Active

```text
ำีสสน
```

Expected:

```text
hello
```

---

### Thai Intended, English Layout Active

```text
l;yfu8iy[
```

Expected:

```text
สวัสดีครับ
```

---

### Russian Intended, English Layout Active

```text
Ghbdtn
```

Expected:

```text
Привет
```

---

### Korean Intended, English Layout Active

```text
dkssudgktpdy
```

Expected:

```text
안녕하세요
```

---

Current solutions typically require users to:

1. Delete the text
2. Change keyboard language
3. Retype everything

This creates frustration and reduces productivity.

---

# Vision

Create the world's most universal keyboard recovery tool that can detect, convert, and fix text typed using incorrect keyboard layouts regardless of language or operating context.

---

# Goals

## Primary Goals

- Universal keyboard layout conversion
- Global hotkey support
- Real-time conversion
- Windows system tray integration
- Ultra-lightweight execution
- Fast conversion response
- Works in all Windows applications

## Secondary Goals

- Auto language detection
- AI-assisted correction
- Custom user mappings
- Cloud synchronization
- Cross-platform support

---

# Core Features

## 1. Selected Text Conversion

Convert highlighted text in any application.

### Workflow

```text
Select Text
    ↓
Press Hotkey
    ↓
Detect Source Layout
    ↓
Convert
    ↓
Replace Text
```

### Example

Input:

```text
l;yfu8iy[
```

Output:

```text
สวัสดีครับ
```

---

## 2. Real-Time Translation Mode

Global monitors keyboard input and converts text as users type.

### Workflow

```text
Key Press
    ↓
Capture Input
    ↓
Detect Layout
    ↓
Translate
    ↓
Display Correct Text
```

---

## 3. Smart Auto Detection

Automatically detects likely layout mistakes.

### Example

Input:

```text
l;yfu8iy[
```

Detection:

```text
English keyboard positions
Thai language pattern
```

Suggestion:

```text
Did you mean:

สวัสดีครับ
```

---

## 4. Drag and Convert

Works everywhere in Windows.

### Usage

```text
Highlight Text
+
Win + Space
```

Result:

```text
Instant Conversion
```

---

## 5. Double Shift Conversion

Users can quickly convert the most recently typed word.

### Example

```text
l;yfu8iy[
```

Press:

```text
Shift + Shift
```

Result:

```text
สวัสดีครับ
```

---

## 6. Clipboard Conversion

### Workflow

```text
Copy
    ↓
Convert
    ↓
Replace Clipboard
```

Useful for applications where direct replacement is restricted.

---

## 7. Floating Suggestion Window

Small popup near cursor displaying:

```text
Converted

l;yfu8iy[
↓
สวัสดีครับ
```

---

## 8. System Tray Mode

```text
Global
├── Convert Selection
├── Toggle Real Time Mode
├── Toggle Auto Detect
├── Supported Layouts
├── Settings
├── Check For Updates
└── Exit
```

---

# Supported Layout Types

## Tier 1
### Physical Keyboard Mapping

Direct key position conversion.

Supported examples:

```text
English
Thai Kedmanee
Russian
Ukrainian
Greek
Arabic
Hebrew
Turkish
Bulgarian
```

### Example

```text
A Key
↓
Character Mapping
↓
Target Layout Character
```

---

## Tier 2
### Composition-Based Languages

Requires syllable composition.

Supported examples:

```text
Korean Hangul
```

### Example

```text
dkssudgktpdy
↓
안녕하세요
```

---

## Tier 3
### IME-Based Languages

Integrates with operating system input methods.

Supported examples:

```text
Chinese Simplified
Chinese Traditional
Japanese
```

### Example

```text
nihao
↓
你好
```

```text
konnichiwa
↓
こんにちは
```

---

# Technical Architecture

## Platform

```text
Windows 10
Windows 11
.NET 8
```

---

## UI

```text
WPF
MVVM
```

---

## Core Components

```text
Global
│
├── UI
│
├── Translation Engine
│
├── Keyboard Hook Service
│
├── Layout Providers
│
├── Auto Detect Engine
│
├── Clipboard Service
│
├── Notification Service
│
├── Hotkey Service
│
├── Settings Service
│
└── Update Service
```

---

# Layout Provider Architecture

```text
ILayoutProvider
```

Capabilities:

```text
Detect Layout
Convert Forward
Convert Reverse
Validate Input
Provide Metadata
```

---

# Project Structure

```text
Global
│
├── Global.UI
│
├── Global.Core
│   ├── Translation
│   ├── Detection
│   ├── Providers
│   └── Settings
│
├── Global.Infrastructure
│   ├── Hooks
│   ├── Hotkeys
│   ├── Clipboard
│   └── Notifications
│
├── Global.Plugins
│   ├── Thai
│   ├── Russian
│   ├── Korean
│   ├── Japanese
│   ├── Chinese
│   └── Custom
│
└── Global.Tests
```

---

# Hotkeys

## Default

```text
Win + Space
```

Convert selected text.

---

## Alternative

```text
Ctrl + `
```

Convert current word.

---

## Alternative

```text
Ctrl + Shift + Space
```

Convert current sentence.

---

## Custom

Users can define any shortcut.

---

# Settings

## General

```text
Start With Windows
Minimize To Tray
Background Operation
Auto Update
```

---

## Conversion

```text
Real Time Conversion
Auto Detection
Double Shift Conversion
Clipboard Mode
```

---

## Layouts

```text
Enable Thai
Enable Russian
Enable Korean
Enable Japanese
Enable Chinese
Enable Custom Layouts
```

---

## Hotkeys

```text
Convert Selection
Convert Word
Convert Sentence
Toggle Real Time Mode
```

---

# Plugin System

Global supports external plugins.

### Examples

```text
Global.Thai
Global.Korean
Global.Japanese
Global.Chinese
Global.Arabic
```

Third-party developers can create additional language packs.

---

# Performance Targets

```text
Startup Time     < 1 second
Memory Usage     < 50 MB
CPU Usage        Near Zero Idle
Conversion Time  < 50 ms
```

---

# MVP Scope

Version 1.0

```text
System Tray Application
Windows Hotkeys
Selected Text Conversion
Real-Time Conversion
English ↔ Thai
English ↔ Russian
English ↔ Korean
Settings Window
Startup With Windows
Plugin Framework
```

---

# Future Roadmap

## Version 2.0

```text
Japanese IME Integration
Chinese IME Integration
Cloud Settings Sync
Auto Updates
Cross-Device Profiles
```

---

## Version 3.0

```text
AI Language Detection
Predictive Correction
Typing Analytics
Learning Engine
Microsoft PowerToys Extension
```

---

# Success Criteria

- Supports major keyboard layouts worldwide
- Works in every Windows application
- Instant layout recovery
- Simple user experience
- Open plugin ecosystem
- Industry-leading conversion accuracy

---

# Target Users

```text
Developers
Students
Office Workers
Call Centers
Data Entry Teams
Translators
Multilingual Professionals
Remote Workers
Global Enterprises
```

---

# Mission

Global aims to become the universal keyboard layout recovery platform for Windows, enabling users around the world to instantly recover text typed with the wrong keyboard layout, regardless of language, country, or application.
