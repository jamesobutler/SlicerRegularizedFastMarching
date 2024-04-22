cmake_minimum_required(VERSION 3.13.4)

project(RegularizedFastMarching)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/jamesobutler/SlicerRegularizedFastMarching#readme")
set(EXTENSION_CATEGORY "Segmentation")
set(EXTENSION_CONTRIBUTORS "Aldrick FAURE, Sandra LEBRETON, Laurent RISSER (CNRS, Toulouse Mathematics Institute / 3IA ANITI), Soleakhena KEN (INSERM, Toulouse University Cancer Institute)")
set(EXTENSION_DESCRIPTION "The RegularizedFastMarching extension in Slicer facilitates efficient semi-automatic segmentation of 3D medical images through the application of regularized fast marching algorithms. Users can manually place seeds or import them from a file, and customize seed labels via CSV files.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/jamesobutler/SlicerRegularizedFastMarching/main/RegularizedFastMarching/Resources/Icons/RegularizedFastMarching.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/jamesobutler/SlicerRegularizedFastMarching/main/Docs/SlicerRFM_README_Fig3.png https://raw.githubusercontent.com/jamesobutler/SlicerRegularizedFastMarching/main/Docs/SlicerRFM_README_Fig2.png https://raw.githubusercontent.com/jamesobutler/SlicerRegularizedFastMarching/main/Docs/SlicerRFM_README_Fig4.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(RegularizedFastMarching)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
