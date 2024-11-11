set(LLVM_LINK_COMPONENTS
  ${LLVM_TARGETS_TO_BUILD}
  Analysis
  CodeGen
  Core
  IPO
  AggressiveInstCombine
  InstCombine
  Instrumentation
  MC
  MCParser
  ObjCARCOpts
  Option
  ScalarOpts
  Support
  TransformUtils
  Vectorize
  TargetParser
)

add_tinylang_tool(tinylang
  Driver.cpp
  )

target_link_libraries(tinylang
  PRIVATE
  tinylangBasic
  tinylangCodeGen
  tinylangLexer
  tinylangParser
  tinylangSema
  )

set_target_properties(tinylang PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/bin"
)

