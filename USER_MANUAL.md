# MALIBU User Manual
## Low-Pass Filter Plugin by Solmar Labs

---

### Table of Contents
1. [Introduction](#introduction)
2. [System Requirements](#system-requirements)
3. [Installation](#installation)
4. [Features Overview](#features-overview)
5. [User Interface](#user-interface)
6. [Parameters](#parameters)
7. [Usage Guide](#usage-guide)
8. [DAW Integration](#daw-integration)
9. [Troubleshooting](#troubleshooting)
10. [Technical Specifications](#technical-specifications)
11. [Support](#support)

---

## Introduction

**MALIBU** is a professional multi-slope low-pass filter plugin designed to bring warmth, character, and precise frequency shaping to your music production. Inspired by the golden sunsets and pristine coastlines of Malibu, this plugin combines cutting-edge digital signal processing with an intuitive, visually stunning interface.

### Key Features
- **Multi-slope filtering**: Choose from 12dB, 24dB, or 48dB per octave slopes
- **Real-time frequency response visualization**: See exactly how your filter affects the audio spectrum
- **Multiple saturation algorithms**: Add harmonic richness with Clean, Warm, or Aggressive saturation
- **Thread-safe design**: Rock-solid stability in professional DAW environments
- **Beautiful Malibu-inspired interface**: Sunset gradient design with smooth animations

---

## System Requirements

### macOS
- **Operating System**: macOS 10.14 (Mojave) or later
- **Architecture**: Intel 64-bit or Apple Silicon (Universal Binary)
- **Formats**: Audio Units (AU), VST3
- **Memory**: 4 GB RAM minimum, 8 GB recommended
- **Disk Space**: 50 MB available space

### Windows
- **Operating System**: Windows 10 (64-bit) or later
- **Architecture**: x64 (64-bit)
- **Formats**: VST3
- **Memory**: 4 GB RAM minimum, 8 GB recommended
- **Disk Space**: 50 MB available space

### Linux
- **Distribution**: Ubuntu 18.04+, Fedora 30+, or equivalent
- **Architecture**: x86_64
- **Formats**: VST3
- **Memory**: 4 GB RAM minimum, 8 GB recommended
- **Disk Space**: 50 MB available space

---

## Installation

### macOS Installation

1. **Download** the `MALIBU_macOS.pkg` installer from the Solmar Labs website
2. **Double-click** the downloaded package file
3. **Follow** the installation wizard instructions
4. **Enter** your administrator password when prompted
5. **Launch** your DAW and scan for new plugins

The installer automatically places the plugin files in:
- Audio Units: `/Library/Audio/Plug-Ins/Components/MALIBU.component`
- VST3: `/Library/Audio/Plug-Ins/VST3/MALIBU.vst3`

### Windows Installation

1. **Download** the `MALIBU_Windows_x64.exe` installer
2. **Right-click** and select "Run as administrator"
3. **Follow** the installation wizard instructions
4. **Choose** your installation directory (default recommended)
5. **Launch** your DAW and rescan plugins

The installer places the plugin in:
- VST3: `C:\Program Files\Common Files\VST3\MALIBU.vst3`

### Linux Installation

1. **Download** the `MALIBU_Linux_x64.tar.gz` package
2. **Extract** the archive: `tar -xzf MALIBU_Linux_x64.tar.gz`
3. **Run** the installation script: `sudo ./install.sh`
4. **Restart** your DAW and rescan plugins

Manual installation:
```bash
mkdir -p ~/.vst3
cp MALIBU.vst3 ~/.vst3/
```

---

## Features Overview

### Advanced Low-Pass Filtering
MALIBU implements state-of-the-art Topology-Preserving Transform (TPT) filter algorithms, providing:
- Musical, analog-like response characteristics
- Stable operation at all cutoff frequencies
- Minimal aliasing and digital artifacts
- Sample-accurate parameter automation

### Real-Time Visual Feedback
The integrated frequency response display shows:
- Current filter curve in real-time
- Visual representation of cutoff frequency and resonance
- Interactive feedback that updates as you adjust parameters
- Smooth animations that enhance the user experience

### Saturation Processing
Three carefully crafted saturation algorithms add harmonic content:
- **Clean**: Transparent processing with subtle harmonic enhancement
- **Warm**: Tube-inspired warmth perfect for melodic content
- **Aggressive**: High-gain saturation for creative sound design

---

## User Interface

### Layout Overview
The MALIBU interface features a beautiful Malibu sunset gradient background with intuitive control placement:

- **Top**: Plugin title "MALIBU" and Solmar Labs logo
- **Center**: Three main rotary controls (Cutoff, Resonance, Drive)
- **Upper Right**: Frequency response visualization
- **Lower Center**: Slope selector (12dB, 24dB, 48dB)
- **Bottom**: Saturation type selector (Clean, Warm, Aggressive)

### Visual Design Elements
- **Sunset Gradient**: Multi-layered color gradient inspired by Malibu sunsets
- **Wave Patterns**: Subtle wave animations reflecting the coastal theme
- **Golden Accents**: Elegant border and highlight colors
- **Professional Typography**: Clean, readable font choices throughout

---

## Parameters

### Cutoff Frequency
- **Range**: 20 Hz to 20 kHz
- **Default**: 1000 Hz
- **Description**: Sets the frequency where the filter begins to attenuate the signal
- **Automation**: Full automation support with sample-accurate timing

### Resonance
- **Range**: 0.0 to 1.0
- **Default**: 0.2
- **Description**: Controls the amount of emphasis at the cutoff frequency
- **Behavior**: Higher values create more pronounced peaks; maximum values can create self-oscillation

### Drive
- **Range**: 0.0 to 1.0
- **Default**: 0.0
- **Description**: Controls the input gain into the saturation stage
- **Effect**: Higher values increase harmonic content and perceived loudness

### Slope Selection
- **Options**: 12dB, 24dB, 48dB per octave
- **Default**: 12dB
- **Description**: Determines how steeply the filter attenuates frequencies above the cutoff
- **Character**: 
  - 12dB: Gentle, musical slope
  - 24dB: Classic analog filter character
  - 48dB: Steep, precise filtering

### Saturation Type
- **Options**: Clean, Warm, Aggressive
- **Default**: Clean
- **Description**: Selects the saturation algorithm
- **Characteristics**:
  - **Clean**: Minimal coloration, transparent processing
  - **Warm**: Even-order harmonics, tube-like warmth
  - **Aggressive**: Asymmetric clipping, enhanced harmonics

---

## Usage Guide

### Basic Low-Pass Filtering

1. **Insert** MALIBU on your desired track
2. **Start** with the default settings (Cutoff: 1000 Hz, Resonance: 0.2)
3. **Adjust** the cutoff frequency to taste
4. **Increase** resonance for more character
5. **Watch** the frequency response display for visual feedback

### Creative Sound Design

1. **Set** a low cutoff frequency (200-500 Hz)
2. **Increase** resonance to near maximum
3. **Select** 48dB slope for aggressive filtering
4. **Add** drive and select "Aggressive" saturation
5. **Automate** the cutoff frequency for dramatic sweeps

### Mixing Applications

1. **Use** gentle settings for transparent high-frequency control
2. **Apply** to drum busses to tame harsh cymbals
3. **Process** vocals to reduce sibilance
4. **Filter** bass instruments to remove mud
5. **Create** movement with subtle automation

### Mastering Considerations

1. **Use** minimal resonance (0.0-0.3) for transparent operation
2. **Choose** 12dB or 24dB slopes for musical character
3. **Keep** drive settings low to maintain dynamics
4. **Monitor** the frequency response display carefully

---

## DAW Integration

### Ableton Live
- Load via **Instruments & Effects Browser** > **Plug-ins** > **Solmar Labs**
- Supports **real-time parameter automation**
- Compatible with **Live's macro controls**

### Logic Pro
- Access via **Mixer** > **Audio FX** > **Solmar Labs** > **MALIBU**
- Full **Logic automation** support
- Compatible with **Logic's plugin delay compensation**

### Pro Tools
- Insert via **Plugin** > **Audio Suite** or **Real-Time**
- Supports **Pro Tools automation** and **control surfaces**
- Compatible with **AAX format** requirements

### Reaper
- Add via **FX** > **VST3** > **Solmar Labs**
- Excellent **parameter automation** capabilities
- Custom **GUI scaling** support

---

## Troubleshooting

### Common Issues

**Plugin doesn't appear in DAW**
- Verify installation directory
- Rescan plugins in your DAW
- Check that your DAW supports VST3/AU format
- Ensure plugin architecture matches DAW (64-bit)

**Crackling or artifacts**
- Increase your DAW's buffer size
- Check CPU usage and close unnecessary applications
- Verify sample rate compatibility
- Reduce resonance if causing instability

**Parameters not responding**
- Check if parameter automation is enabled
- Verify MIDI controller mappings
- Restart your DAW and reload the plugin
- Check for plugin conflicts

**Visual display issues**
- Update graphics drivers
- Disable graphics acceleration if available
- Try different buffer sizes
- Check monitor resolution compatibility

### Performance Optimization

**Reduce CPU usage**:
- Use lower buffer sizes only when necessary
- Disable visual display when not needed
- Limit the number of instances per project
- Consider rendering/bouncing heavily processed tracks

**Improve stability**:
- Keep your DAW updated
- Use the latest plugin version
- Close unnecessary background applications
- Monitor system resources during recording

### Contact Support

If you continue experiencing issues:
- Email: support@solmarlabs.com
- Include your system specifications
- Describe the exact steps to reproduce the issue
- Attach any relevant error messages or crash logs

---

## Technical Specifications

### Audio Processing
- **Sample Rate Support**: 44.1 kHz to 192 kHz
- **Bit Depth**: 32-bit floating point internal processing
- **Latency**: Zero latency (real-time processing)
- **CPU Usage**: Optimized for low CPU consumption

### Filter Implementation
- **Algorithm**: Topology-Preserving Transform (TPT)
- **Oversampling**: Internal 2x oversampling for saturation stage
- **Frequency Response**: Flat response outside filter band
- **THD+N**: <0.01% at nominal levels

### Automation
- **Parameter Count**: 5 automatable parameters
- **Resolution**: Sample-accurate parameter updates
- **Smoothing**: Optimized parameter smoothing to prevent zipper noise
- **MIDI Learn**: Standard MIDI CC mapping support

---

## Support

### Documentation
- Complete user manual (this document)
- Quick start guide
- Video tutorials (available on website)
- FAQ section

### Technical Support
- **Email**: support@solmarlabs.com
- **Response Time**: 24-48 hours
- **Languages**: English
- **Coverage**: Installation, usage, troubleshooting

### Updates
- Automatic update notifications
- Free updates for the first year
- Version history and changelog available
- Beta testing program for advanced users

### Community
- User forums at solmarlabs.com/community
- Share presets and techniques
- Connect with other MALIBU users
- Feature requests and feedback

---

**MALIBU** is a product of **Solmar Labs**. 
Copyright © 2025 Solmar Labs. All rights reserved.

For the latest information, visit: [www.solmarlabs.com](http://www.solmarlabs.com)
