# DiligentEngineCI
CI builds of DiligentEngine for x86 platform

# How to use

See [cmake](cmake) folder for include files. Then in your own library `CMakeLists.txt` do:

```cmake
find_package(DENGINE REQUIRED)

...

target_link_libraries(<libname>
  ...
  DENGINE::DENGINE
  DENGINE::GLEW
  DENGINE::GLSLANG
  DENGINE::HLSL
  DENGINE::OGLCOMPILER
  DENGINE::OSDEPENDENT
  DENGINE::SPIRVCROSSCORE
  DENGINE::SPIRVTOOLSOPT
  DENGINE::SPIRVTOOLS
  DENGINE::SPIRV
  DENGINE::TOOLS
  DENGINE::LIBPNG
  DENGINE::LIBJPEG
  DENGINE::LIBTIFF
  DENGINE::ZLIB
	...
)

target_compile_options(<libname>
	...
  PRIVATE /DPLATFORM_WIN32
  PRIVATE /DD3D11_SUPPORTED
  PRIVATE /DD3D12_SUPPORTED
  PRIVATE /DGL_SUPPORTED
  PRIVATE /DVULKAN_SUPPORTED
  ...
)
```