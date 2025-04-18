add_lldb_unittest(SymbolTests
  JSONSymbolTest.cpp
  LineTableTest.cpp
  LocateSymbolFileTest.cpp
  MangledTest.cpp
  PostfixExpressionTest.cpp
  SymbolTest.cpp
  SymtabTest.cpp
  TestTypeSystem.cpp
  TestTypeSystemClang.cpp
  TestClangASTImporter.cpp
  TestDWARFCallFrameInfo.cpp
  TestType.cpp
  TestLineEntry.cpp
  UnwindPlanTest.cpp

  LINK_LIBS
    lldbCore
    lldbHost
    lldbSymbol
    lldbUtilityHelpers
    lldbPluginObjectFileELF
    lldbPluginObjectFileMachO
    lldbPluginSymbolFileDWARF
    lldbPluginSymbolFileSymtab
    lldbPluginTypeSystemClang
    LLVMTestingSupport
  )

set(test_inputs
  inlined-functions.yaml
  )
add_unittest_inputs(SymbolTests "${test_inputs}")
