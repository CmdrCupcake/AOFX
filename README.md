# AMD AOFX

![AMD AOFX](http://gpuopen-effects.github.io/media/effects/aofx_thumbnail.png)

The AOFX library provides a scalable and GCN-optimized ambient occlusion (AO) solution.

<div>
  <a href="https://github.com/GPUOpen-Effects/AOFX/releases/latest/"><img src="http://gpuopen-effects.github.io/media/latest-release-button.svg" alt="Latest release" title="Latest release"></a>
</div>

Currently, the library supports the High Definition Ambient Occlusion (HDAO) kernel and implements a variety of options:
* Pixel shader and compute shader implementations
* Multi-layer approach that provides fine details and smooth, alias-free global ambient occlusion
* Takes depth buffer or depth+normal buffers as input
* Supports input de-interleaving and downscaling
* Fast, separable, depth-guided bilateral blur

The AOFX library can also serve as a sandbox for experiments with other AO techniques

### Prerequisites
* AMD Radeon&trade; GCN-based GPU (HD 7000 series or newer)
  * Or other DirectX&reg; 11 compatible discrete GPU with Shader Model 5 support 
* 64-bit Windows&reg; 7 (SP1 with the [Platform Update](https://msdn.microsoft.com/en-us/library/windows/desktop/jj863687.aspx)), Windows&reg; 8.1, or Windows&reg; 10
* Visual Studio&reg; 2015 or Visual Studio&reg; 2017

### Getting started
* Visual Studio solutions for VS2015 or VS2017 can be found in the `amd_aofx_sample\build` directory.
* There are also solutions for just the core library in the `amd_aofx\build` directory.
* Additional documentation is available in the `amd_aofx\doc` directory.

### Premake
The Visual Studio solutions and projects in this repo were generated with Premake. If you need to regenerate the Visual Studio files, double-click on `gpuopen_geometryfx_update_vs_files.bat` in the `premake` directory.

For Visual Studio 2015 and 2017, this version of Premake adds the `WindowsTargetPlatformVersion` element to the project file to specify which version of the Windows SDK will be used. To change `WindowsTargetPlatformVersion` for Visual Studio 2015 and 2017, change the value for `_AMD_WIN_SDK_VERSION` in `premake\amd_premake_util.lua` and regenerate the Visual Studio files.

### Third-Party Software
* DXUT is distributed under the terms of the MIT License. See `framework\d3d11\dxut\MIT.txt`.
* Premake is distributed under the terms of the BSD License. See `premake\LICENSE.txt`.

DXUT is only used by the sample, not the core library. Only first-party software (specifically `amd_aofx` and `amd_lib`) is needed to build the AOFX library.

### Attribution
* AMD, the AMD Arrow logo, Radeon, and combinations thereof are either registered trademarks or trademarks of Advanced Micro Devices, Inc. in the United States and/or other countries.
* Microsoft, DirectX, Visual Studio, and Windows are either registered trademarks or trademarks of Microsoft Corporation in the United States and/or other countries.
