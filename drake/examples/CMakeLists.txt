
add_matlab_test(NAME examples/CubicPolynomialExample.findFixedPointTest COMMAND CubicPolynomialExample.findFixedPointTest)
add_matlab_test(NAME examples/CubicPolynomialExample.animate COMMAND CubicPolynomialExample.animate)
add_matlab_test(NAME examples/CubicPolynomialExample.sosExample COMMAND CubicPolynomialExample.sosExample)
add_matlab_test(NAME examples/CubicPolynomialExample.run COMMAND CubicPolynomialExample.run)
add_matlab_test(NAME examples/DoubleIntegrator.runDircol COMMAND DoubleIntegrator.runDircol)
add_matlab_test(NAME examples/DoubleIntegrator.runDirtran COMMAND DoubleIntegrator.runDirtran)
add_matlab_test(NAME examples/DoubleIntegrator.runConvexDirtran COMMAND DoubleIntegrator.runConvexDirtran)
add_matlab_test(NAME examples/DoubleIntegrator.runValueIteration COMMAND DoubleIntegrator.runValueIteration)

add_matlab_test(NAME examples/GridWorld.runValueIteration COMMAND GridWorld.runValueIteration)
add_matlab_test(NAME examples/GridWorld.drawBoard COMMAND GridWorld.drawBoard)

add_matlab_test(NAME examples/LinearGaussianExample.run COMMAND LinearGaussianExample.run)

add_matlab_test(NAME examples/SineSys.runTaylor COMMAND SineSys.runTaylor)
add_matlab_test(NAME examples/SineSys.runTrigPolyVectorFields COMMAND SineSys.runTrigPolyVectorFields)
add_matlab_test(NAME examples/SineSys.run COMMAND SineSys.run)

add_matlab_test(NAME examples/VanDerPol.particleDemo COMMAND VanDerPol.particleDemo)
add_matlab_test(NAME examples/VanDerPol.runDircol COMMAND VanDerPol.runDircol)
add_matlab_test(NAME examples/VanDerPol.phasePortrait COMMAND VanDerPol.phasePortrait)
add_matlab_test(NAME examples/VanDerPol.run COMMAND VanDerPol.run)

add_matlab_test(NAME examples/commonLyapunovForLinearSystems COMMAND commonLyapunovForLinearSystems)


# recurse into all example subdirectories
# note: the GLOB workflow is typically not recommended due to the fact that cmake will not be able
# to detect changes, but we currently support users adding contributed examples by installing
# directly into examples/MY_EXAMPLE .  See #1939
file(GLOB children *)
foreach(child ${children})
  if(IS_DIRECTORY ${child})
    add_subdirectory(${child})
  endif()
endforeach()
