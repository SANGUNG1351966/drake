
add_matlab_test(NAME examples/UnderwaterAcrobot/runLQR COMMAND runLQR)
add_matlab_test(NAME examples/UnderwaterAcrobot/runPassive COMMAND runPassive)
add_matlab_test(NAME examples/UnderwaterAcrobot/runPassiveURDF COMMAND runPassiveURDF)
add_matlab_test(NAME examples/UnderwaterAcrobot/runSwingUp COMMAND runSwingUp)
add_matlab_test(NAME examples/UnderwaterAcrobot/runURDFandAnalyticSoln COMMAND runURDFandAnalyticSoln)

add_subdirectory(test)
