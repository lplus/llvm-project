add_mlir_dialect_library(MLIRStandardOpsTransforms
  ExpandAtomic.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/StandardOps/Transforms

  DEPENDS
  MLIRStandardTransformsIncGen
  )
target_link_libraries(MLIRStandardOpsTransforms
  PUBLIC
  MLIRIR
  MLIRPass
  MLIRStandardOps
  MLIRSupport
  MLIRTransforms 
  LLVMSupport
  )
