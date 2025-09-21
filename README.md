# MALIBU - Professional Multi-Slope Low-Pass Filter Plugin

**MALIBU** is a professional-grade low-pass filter audio plugin with selectable filter slopes, real-time frequency response visualization, and multiple saturation algorithms. Inspired by the golden sunsets and pristine coastlines of Malibu, this plugin combines cutting-edge digital signal processing with a visually stunning interface.

## 🎯 Features

### Advanced Low-Pass Filtering
- **Multiple Filter Slopes**: 12dB/octave, 24dB/octave, and 48dB/octave
- **TPT (Topology-Preserving Transform) Filters**: State-of-the-art zero-delay feedback implementation
- **Resonance Control**: From gentle Butterworth response to self-oscillation
- **Cutoff Range**: 20Hz to 20kHz with professional logarithmic scaling
- **Sample-Accurate Parameter Smoothing**: Click-free parameter changes

### Saturation Processing
- **Three Saturation Algorithms**:
  - **Clean**: Transparent processing with minimal coloration
  - **Warm**: Tube-inspired warmth with even-order harmonics
  - **Aggressive**: High-gain saturation for creative sound design
- **Drive Control**: 0.0 to 1.0 range for input gain into saturation stage
- **Internal Oversampling**: Prevents aliasing in saturation stage

### Visual Feedback
- **Real-Time Frequency Response**: Professional-grade visualization
- **Logarithmic Frequency Scale**: Industry standard 20Hz-20kHz display  
- **dB Magnitude Scale**: -60dB to 0dB range with grid references
- **Interactive Parameter Feedback**: Visual updates as you adjust controls
- **Smooth Animations**: Enhanced user experience with fluid transitions

### Professional Interface
- **Malibu-Inspired Design**: Beautiful sunset gradient background with wave patterns
- **Rotary Knob Controls**: Intuitive parameter adjustment with custom look-and-feel
- **Slope Selection Interface**: Easy switching between filter types
- **Saturation Type Selector**: Quick access to different saturation algorithms
- **Company Branding**: Elegant Solmar Labs logo integration
- **Thread-Safe Architecture**: Rock-solid stability in professional DAW environments

## 🏗️ Technical Architecture

### TPT Filter Implementation

MALIBU uses advanced TPT (Topology-Preserving Transform) state variable filters to achieve different slopes:

- **12dB/octave (2-pole)**: Single TPT-SVF stage
- **24dB/octave (4-pole)**: Two cascaded TPT-SVF stages  
- **48dB/octave (8-pole)**: Four cascaded TPT-SVF stages

Each filter stage implements the TPT zero-delay feedback topology:
```
u = (input - R * s1 - s2) * h
v1 = u * g
v2 = v1 + s1
v3 = v2 * g + s2
```

### Key Components

1. **TPTFilterProcessor**: Advanced zero-delay feedback filter engine with saturation
2. **FrequencyResponseDisplay**: Real-time visualization component with thread-safe communication
3. **SlopeSelector**: Interactive slope selection interface
4. **SaturationTypeSelector**: Saturation algorithm selection interface
5. **PluginProcessor**: JUCE audio processor with parameter management
6. **PluginEditor**: Complete GUI implementation with Malibu-inspired design

### Parameter Management

- **Cutoff Frequency**: 20Hz - 20kHz, logarithmic scaling with sample-accurate smoothing
- **Resonance**: 0.0 - 1.0, linear scaling with geometric Q distribution for multi-stage stability
- **Drive**: 0.0 - 1.0, input gain control for saturation stage
- **Slope Selection**: Discrete choice between 12dB, 24dB, 48dB per octave
- **Saturation Type**: Clean, Warm (Tube), Aggressive algorithms
- **Thread-Safe Communication**: Lock-free FIFO for audio/UI thread separation
5. **PluginEditor**: Complete GUI implementation

### Parameter Management

- **Cutoff Frequency**: 20Hz - 20kHz, logarithmic scaling
- **Resonance**: 0.5 - 10.0, linear scaling (Q factor)
- **Slope Selection**: Discrete choice between three options
- **Automated Synchronization**: GUI ↔ DSP parameter binding

## 🚀 Getting Started

### Prerequisites

- **macOS 10.15+** (Catalina or later)
- **Xcode 12+** with command line tools
- **CMake 3.22+**
- **Git** for JUCE framework download

### Quick Setup

1. **Clone and setup**:
   ```bash
   cd /your/desired/path
   git clone [your-repo-url] MultiSlopeFilter
   cd MultiSlopeFilter
   chmod +x setup.sh
   ./setup.sh
   ```

2. **Build the plugin**:
   ```bash
   cd build
   cmake --build . --config Release
   ```

3. **Test the plugin**:
   - **Standalone**: Run `MultiSlopeFilter_artefacts/Release/Standalone/MultiSlopeFilter.app`
   - **VST3**: Copy from `MultiSlopeFilter_artefacts/Release/VST3/` to your VST3 folder
   - **AU**: Copy from `MultiSlopeFilter_artefacts/Release/AU/` to your AU folder

## 🎛️ Usage Guide

### Basic Operation

1. **Select Filter Slope**: Use the buttons to choose 12dB, 24dB, or 48dB/octave
2. **Set Cutoff Frequency**: Adjust the blue rotary knob (20Hz - 20kHz)
3. **Control Resonance**: Use the orange knob for filter emphasis (0.5 - 10.0)
4. **Monitor Response**: Watch the cyan curve update in real-time

### Creative Applications

- **Gentle Filtering**: 12dB slope with low resonance for musical cuts
- **Aggressive Filtering**: 48dB slope for dramatic frequency removal
- **Resonant Sweeps**: High resonance with cutoff automation for classic effects
- **Mix Bus Filtering**: Subtle high-frequency control on full mixes
- **Creative Sound Design**: Self-oscillation effects with maximum resonance

### Parameter Ranges

| Parameter | Range | Default | Description |
|-----------|-------|---------|-------------|
| Cutoff | 20Hz - 20kHz | 1000Hz | Filter cutoff frequency |
| Resonance | 0.0 - 1.0 | 0.2 | Filter emphasis at cutoff |
| Drive | 0.0 - 1.0 | 0.0 | Saturation input gain |
| Slope | 12/24/48 dB/oct | 12dB | Filter rolloff steepness |
| Saturation | Clean/Warm/Aggressive | Clean | Harmonic processing type |

## 🔧 Development Notes

### Filter Design Principles

The multi-slope implementation follows these key principles:

1. **Stability**: Each filter stage is independently stable
2. **Consistency**: All slopes use the same filter topology
3. **Performance**: Optimized for real-time audio processing
4. **Precision**: High-resolution parameter control

### Performance Characteristics

- **CPU Usage**: Scales linearly with slope selection
- **Latency**: Zero-latency processing (no look-ahead)
- **Memory**: Minimal state per filter stage
- **Precision**: 32-bit floating-point throughout

### Code Organization

```
Source/
├── PluginProcessor.h/cpp           # Main audio processor with parameter management
├── PluginEditor.h/cpp              # GUI implementation with Malibu-inspired design
├── TPTFilterProcessor.h/cpp        # Advanced TPT filter engine with saturation
├── FrequencyResponseDisplay.h/cpp  # Real-time visualization with thread safety
├── SlopeSelector.h/cpp             # Slope selection interface
├── SaturationTypeSelector.h/cpp    # Saturation algorithm selection
└── BinaryData.h/cpp                # Embedded company logo resources
```

## 📚 Learning Objectives

This project demonstrates several key audio plugin development concepts:

### Advanced DSP Concepts
- **TPT Filter Design**: Zero-delay feedback topology for stable resonance
- **Cascaded Filter Architecture**: Building complex responses from multiple stages
- **Geometric Q Distribution**: Maintaining stability in multi-stage configurations
- **Sample-Accurate Parameter Smoothing**: Preventing audio artifacts during automation
- **Saturation Algorithms**: Multiple harmonic processing techniques
- **Thread-Safe Real-Time Processing**: Lock-free communication between audio and UI

### JUCE Framework Mastery
- **AudioProcessor Architecture**: Professional plugin structure with parameter trees
- **Custom GUI Components**: Building specialized interfaces with custom look-and-feel
- **Real-Time Graphics**: Efficient visualization with thread-safe data sharing
- **Parameter Management**: Value trees with automatic synchronization
- **Multi-Format Building**: VST3, AU, and Standalone application support

### Software Engineering
- **Lock-Free Programming**: Real-time safe communication between threads
- **Template Usage**: Generic programming for filter stages and visualization
- **Performance Optimization**: Meeting real-time audio constraints
- **Cross-Platform Development**: macOS, Windows, and Linux compatibility
- **Professional UI Design**: Beautiful, functional interfaces with branding integration

## 🛠️ Customization Ideas

### Immediate Enhancements
- **Additional Filter Types**: High-pass, band-pass, notch filters using TPT topology
- **Envelope Follower**: Dynamic cutoff based on input level analysis
- **MIDI Control**: Note-based cutoff frequency control and velocity sensitivity
- **Preset System**: Save/recall complete plugin configurations
- **Additional Saturation Models**: Tape, valve, and transistor emulations

### Advanced Features  
- **Adaptive Oversampling**: Dynamic oversampling based on drive and frequency content
- **Multi-Band Processing**: Independent filtering per frequency band
- **Modulation Sources**: Built-in LFOs and envelopes for parameter automation
- **Spectral Analysis**: Real-time input spectrum display alongside filter response
- **Zero-Latency Lookahead**: Advanced parameter smoothing for automation

### Creative Extensions
- **Formant Filtering**: Vocal-like filter responses with multiple peaks
- **Comb Filtering**: Resonant delay-based effects integrated with main filter
- **Morphing Filters**: Smooth transitions between different filter characteristics
- **Granular Integration**: Per-grain filtering in granular synthesis applications
- **AI-Powered Presets**: Machine learning-based automatic parameter adjustment

## 🐛 Troubleshooting

### Build Issues

**"JuceHeader.h not found"**
- Run `./setup.sh` to download JUCE framework
- Ensure JUCE directory exists in project root
- Check CMakeLists.txt JUCE path configuration

**"Cannot find BinaryData.h"**
- Ensure BinaryData.cpp is included in CMakeLists.txt target_sources
- Run CMake configure step to generate binary data files
- Check that logo files are properly embedded

### Runtime Issues

**Plugin not loading in DAW**
- Check plugin format compatibility (VST3 vs AU)
- Verify installation path matches DAW expectations
- Run Audio Unit Validation (AU plugins on macOS)
- Check system architecture (64-bit) compatibility

**Crackling or artifacts in saturation**
- Reduce drive amount or switch to Clean saturation
- Check for clipping in input signal chain
- Verify sample rate compatibility with DAW
- Test with different buffer sizes

**Thread safety or stability issues**
- Ensure you're using the latest version with lock-free communication
- Check for excessive parameter automation rates
- Verify DAW compatibility with VST3/AU standards
- Test in standalone mode to isolate DAW-specific issues

## 🎓 Next Steps

Based on the ROADMAP.md, consider these progression paths:

1. **Enhance Current Filter**: Add more filter types and modulation
2. **Build Different Effects**: Distortion, delay, compression
3. **Study Advanced DSP**: Convolution, spectral processing, synthesis
4. **Professional Features**: Presets, MIDI learn, oversampling
5. **Performance Optimization**: SIMD, threading, profiling

## 📖 Resources

### JUCE Learning
- [JUCE Tutorials](https://juce.com/learn/tutorials)
- [JUCE Documentation](https://docs.juce.com/)
- [JUCE Forum](https://forum.juce.com/)

### DSP Theory  
- "The Scientist and Engineer's Guide to DSP" (free online)
- "Designing Audio Effect Plugins in C++" by Will Pirkle
- "DAFX: Digital Audio Effects" by Udo Zölzer

### Audio Programming
- [Music DSP Archive](https://www.musicdsp.org/)
- [KVR Audio Developer Challenge](https://www.kvraudio.com/)
- [r/WeAreTheMusicMakers](https://www.reddit.com/r/WeAreTheMusicMakers/)

---

## 📄 License

**Copyright © 2025 Solmar Labs. All rights reserved.**

This project is created for educational and commercial purposes. MALIBU is a trademark of Solmar Labs. Please respect the JUCE licensing terms for any commercial usage.

## 🤝 Contributing

This is a professional plugin project - feel free to experiment, build upon the foundation, and create your own variations!

**Happy filtering! 🎵**
