add_executable (calc
  Calc.cpp
  CodeGen.cpp
  Lexer.cpp
  Parser.cpp
  Sema.cpp
  )
target_link_libraries(calc PRIVATE ${llvm_libs})
set_target_properties(calc PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin
)
