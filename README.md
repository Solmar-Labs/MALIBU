# MALIBU v1.0.0 Release Notes
## Professional Multi-Slope Low-Pass Filter Plugin

**Release Date:** September 20, 2025  
**Version:** 1.0.0  
**Developer:** Solmar Labs  

---

## 🎉 Initial Release

We're thrilled to announce the first release of **MALIBU**, a professional multi-slope low-pass filter plugin that brings the warmth and beauty of Malibu sunsets to your music production workflow.

## ✨ Key Features

### Advanced Filtering
- **Multi-slope filtering**: Choose from 12dB, 24dB, or 48dB per octave slopes
- **Topology-Preserving Transform (TPT) algorithms**: State-of-the-art digital signal processing
- **Sample-accurate automation**: Smooth parameter changes without artifacts
- **Wide frequency range**: 20 Hz to 20 kHz with musical response characteristics

### Real-Time Visualization
- **Interactive frequency response display**: See exactly how your filter affects the audio spectrum
- **Live parameter feedback**: Visual updates as you adjust controls
- **Smooth animations**: Enhanced user experience with fluid visual transitions

### Saturation Processing
- **Three saturation algorithms**:
  - **Clean**: Transparent processing with subtle harmonic enhancement
  - **Warm**: Tube-inspired warmth perfect for melodic content  
  - **Aggressive**: High-gain saturation for creative sound design
- **Internal oversampling**: Prevents aliasing in saturation stage

### Professional Interface
- **Malibu-inspired design**: Beautiful sunset gradient background with wave patterns
- **Intuitive controls**: Large, easy-to-use rotary knobs with precise control
- **Company branding**: Elegant Solmar Labs logo integration
- **Responsive layout**: Optimized for various screen sizes

### Rock-Solid Stability
- **Thread-safe architecture**: Separate audio and UI threads prevent crashes
- **Lock-free communication**: High-performance FIFO buffers for real-time operation
- **Extensive testing**: Validated across multiple DAWs and system configurations

## 🖥️ System Requirements

### macOS
- **OS**: macOS 10.14 (Mojave) or later
- **Architecture**: Intel 64-bit or Apple Silicon (Universal Binary)
- **Formats**: Audio Units (AU), VST3
- **RAM**: 4 GB minimum, 8 GB recommended

### Windows
- **OS**: Windows 10 (64-bit) or later
- **Architecture**: x64 (64-bit)
- **Formats**: VST3
- **RAM**: 4 GB minimum, 8 GB recommended

### Linux
- **Distribution**: Ubuntu 18.04+, Fedora 30+, or equivalent
- **Architecture**: x86_64
- **Formats**: VST3
- **RAM**: 4 GB minimum, 8 GB recommended

## 📦 What's Included

### Plugin Files
- **macOS**: AU component and VST3 plugin with Universal Binary support
- **Windows**: VST3 plugin with x64 architecture
- **Linux**: VST3 plugin for x86_64 systems

### Documentation
- **Complete User Manual**: Comprehensive guide with usage examples and best practices
- **Quick Start Guide**: Get up and running in 5 minutes
- **Technical Specifications**: Detailed specs for audio engineers

### Installation
- **macOS**: Professional .pkg installer with code signing support
- **Windows**: NSIS installer with Add/Remove Programs integration
- **Linux**: .tar.gz package with automatic installation script, .deb and .rpm specs

## 🎛️ Parameter Overview

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| **Cutoff** | 20 Hz - 20 kHz | 1000 Hz | Filter cutoff frequency |
| **Resonance** | 0.0 - 1.0 | 0.2 | Emphasis at cutoff frequency |
| **Drive** | 0.0 - 1.0 | 0.0 | Saturation input gain |
| **Slope** | 12/24/48 dB | 12 dB | Filter steepness per octave |
| **Saturation** | Clean/Warm/Aggressive | Clean | Harmonic processing type |

## 🎵 Compatibility

### Supported DAWs
- **Logic Pro & GarageBand** (AU format)
- **Pro Tools** (VST3 format)
- **Ableton Live** (VST3 format)
- **Reaper** (AU/VST3 formats)
- **Cubase & Nuendo** (VST3 format)
- **Studio One** (VST3 format)
- **Bitwig Studio** (VST3 format)
- **And many more AU/VST3 compatible applications**

### Sample Rates
- 44.1 kHz
- 48 kHz
- 88.2 kHz
- 96 kHz
- 176.4 kHz
- 192 kHz

## 🛠️ Installation Instructions

### macOS
1. Download `MALIBU_v1.0.0_macOS.pkg`
2. Double-click and follow the installer
3. Restart your DAW and rescan plugins

### Windows
1. Download `MALIBU_v1.0.0_Windows_x64.exe`
2. Run as administrator and follow the installer
3. Restart your DAW and rescan plugins

### Linux
1. Download `MALIBU_v1.0.0_Linux_x64.tar.gz`
2. Extract and run `./install.sh`
3. Restart your DAW and rescan plugins

## 🔧 Technical Highlights

- **Zero-latency processing**: Real-time operation without delay
- **32-bit floating point**: Internal processing for maximum precision
- **Optimized performance**: Low CPU usage even with multiple instances
- **Parameter smoothing**: Prevents zipper noise during automation
- **Stable at all settings**: No instability even at extreme parameter values

## 🎨 Usage Examples

### Mixing Applications
- **Gentle high-frequency control**: Set cutoff to 8-12 kHz with minimal resonance
- **Drum bus processing**: Tame harsh cymbals and hi-hats
- **Vocal de-essing**: Reduce sibilance with surgical precision
- **Bass management**: Remove mud and unwanted low-end content

### Creative Sound Design
- **Filter sweeps**: Automate cutoff with high resonance for dramatic effects
- **Vintage warmth**: Use Warm saturation with gentle filtering
- **Aggressive textures**: Combine steep slopes with Aggressive saturation
- **Movement and interest**: Subtle automation brings static sounds to life

### Mastering Applications
- **Transparent control**: Clean saturation with gentle slopes
- **Frequency shaping**: Precise control over the high-frequency spectrum
- **Harmonic enhancement**: Subtle warmth without compromising dynamics

## 📋 Release Checklist Status

- ✅ **Core Development**: Plugin functionality and features complete
- ✅ **Thread Safety**: Rock-solid stability in professional environments  
- ✅ **User Interface**: Beautiful, intuitive design with company branding
- ✅ **Documentation**: Comprehensive manual and quick start guide
- ✅ **Multi-Platform**: macOS, Windows, and Linux support
- ✅ **Professional Installers**: Platform-specific installation packages
- ⏳ **Code Signing**: Certificates and notarization for trusted distribution
- ⏳ **Quality Assurance**: Extensive testing across DAWs and systems

## 🆘 Support & Resources

### Getting Help
- **Email Support**: support@solmarlabs.com
- **Documentation**: Complete user manual included
- **Website**: https://solmarlabs.com
- **Response Time**: 24-48 hours for technical support

### Community
- **User Forums**: Share presets and techniques
- **Feature Requests**: Help shape future development
- **Beta Testing**: Early access to new features

## 🔄 Future Development

We're committed to continuous improvement of MALIBU. Planned features include:
- Additional filter types (high-pass, band-pass, notch)
- Preset management system
- MIDI learn functionality
- Additional saturation algorithms
- Performance optimizations

## 📄 Legal

**Copyright © 2025 Solmar Labs. All rights reserved.**

MALIBU is a trademark of Solmar Labs. VST is a trademark of Steinberg Media Technologies GmbH. Audio Units is a trademark of Apple Inc. All other trademarks are the property of their respective owners.

---

**Thank you for choosing MALIBU!** We're excited to hear what you create with our plugin. Your feedback and support drive our continued development of professional audio tools.

*For the latest updates and information, visit: https://solmarlabs.com*
