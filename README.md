# Fast Calib - A Geometric Camera Calibration Solution

<p align="center">
	<img src="https://img.shields.io/badge/Release-0.0.1-blue.svg?style=flat" height="20" />
	&nbsp;
	<img src="https://img.shields.io/badge/License-BSD%203-blue.svg?style=flat" height="20" />
</p>

<p align="center">
	<img src="https://github.com/fast-calib/fast-calib/workflows/Build%20on%20Ubuntu/badge.svg" height="20" />
	&nbsp;
	<img src="https://github.com/fast-calib/fast-calib/workflows/Build%20on%20MacOS/badge.svg" height="20" />
	&nbsp;
	<img src="https://github.com/fast-calib/fast-calib/workflows/Build%20on%20Windows/badge.svg" height="20" />
</p>

## <a name="overview">Contents</a>

<h3>
	<ol>
		<li><a href="#overview">Overview</a></li>
		<li><a href="#references">References</a></li>
		<li><a href="#quick_start_guide">Quick Start Guide</a></li>
		<li><a href="#building">Building</a></li>
		<li><a href="#detailed_guide">Detailed Guide</a></li>
	</ol>
</h3>

## <a name="overview">1. Overview</a>

The Fast Calibration (fast-calib) is a tool for **geometric camera calibration**. The focus is on **speed**, **accuracy**, and **easy deployment**.

It supports calibration with **generic camera models**, which can fit nearly every camera and allow for highly accurate calibration.

## <a name="references">2. References</a>

This software is based on the [Camera Calibration project](https://github.com/puzzlepaint/camera_calibration) from [@puzzlepaint](https://github.com/puzzlepaint). The original repository contains the implementation of the 2019 paper:

[Thomas Schöps, Viktor Larsson, Marc Pollefeys, Torsten Sattler, "Why Having 10,000 Parameters in Your Camera Model is Better Than Twelve", arXiv 2019](https://arxiv.org/abs/1912.02908).

## <a name="building">3. Quick Start Guide</a>

## <a name="building">4. Building</a>

### <a name="building_dependencies">4.1 Dependencies</a>

| Dependency | Version | Status    |
| ---------- | ------- | --------- |
| Eigen      | 3.X     | Mandatory |

### <a name="building_guides">4.2 Installation guides</a>

#### <a name="guide_ubuntu">4.2.1 Ubuntu</a>

The application was built and tested on Ubuntu 18.04 LTS and Ubuntu 20.04 LTS. 

#### <a name="guide_macos">4.2.2 MacOS</a>

The application was built and tested on MacOS Catalina 10.15.7. 

#### <a name="guide_ubguide_windowsuntu">4.2.3 Windows</a>

This project was built and tested on Windows 10 with Visual Studio 2019 x64.

### <a name="building_testing">4.3 Testing</a>

## <a name="references">5. Detailed guide</a>

## <a name="todo">6. TODO</a>

### What do we want

- Cross-platform build
- Continuous integration
- Documentation
- Low number of dependencies (Optional CUDA, Optional SuiteSparse, ...)

### What do we need

- Setup CMake project
- Setup CI in Github
- Look into documentation builds (Doxygen, readthedocs website, ...)
- Study and understand the original project

### Tasks

- Create dummy CMake project with Eigen dependency
- Setup CI following a tutorial
- Setup documentation build
- Study and understand original project
- Decide on the project structure
- Setup vcpkg as git submodule for CI and Windows build
