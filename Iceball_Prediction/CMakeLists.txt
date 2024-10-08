cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(PredictIceball)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/lassoan/SlicerMONAIAuto3DSeg")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Andras Lasso (PerkLab, Queen's University)" "Andres Diaz Pinto (NVIDIA & KCL)" "Rudolf Bumm (KSGR Switzerland)")
set(EXTENSION_DESCRIPTION "Run MONAI Auto3DSeg fully automatic AI segmentation in 3D Slicer.")
set(EXTENSION_ICONURL "https://github.com/nayanimodugula/AutomatedSegmentation/blob/main/logo.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/lassoan/SlicerMONAIAuto3DSeg/main/Screenshot01.jpg https://raw.githubusercontent.com/lassoan/SlicerMONAIAuto3DSeg/main/Screenshot02.jpg https://raw.githubusercontent.com/lassoan/SlicerMONAIAuto3DSeg/main/Screenshot03.jpg https://raw.githubusercontent.com/lassoan/SlicerMONAIAuto3DSeg/main/Screenshot04.jpg https://raw.githubusercontent.com/lassoan/SlicerMONAIAuto3DSeg/main/Screenshot05.jpg")
set(EXTENSION_DEPENDS "PyTorch")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(PredictIceball)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
