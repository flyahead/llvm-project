set(LLVM_LINK_COMPONENTS
  ${LLVM_TARGETS_TO_BUILD}
  support
  )

add_clang_tool(clang-extdef-mapping
  ClangExtDefMapGen.cpp
  )

clang_target_link_libraries(clang-extdef-mapping
  PRIVATE
  clangAST
  clangBasic
  clangCrossTU
  clangFrontend
  clangSerialization
  clangTooling
  )
