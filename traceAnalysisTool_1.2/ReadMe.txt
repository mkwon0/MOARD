﻿The README for the traceAnalysisTool
Summary:
- this traceAnalysisTool is developed to analyze the trace generated by LLVM Tracer, 
  which is a trace generation tool based on LLVM IR. More specifically, the 
  traceAnaylsisTool is to count the fault vulnerability rate of the source program 
  of the input program.

- The input trace is produced by the LLVM Tracer;

- The trace of the target program is then read into the traceAnaylsisTool;

- A counter is created to count the fault masking events happening on the target 
  data structure;

- A proposed metric is used for quantify the aDVF of the target data structure of 
  the input progam.

Scripts to execution:
a. oneFileRunning.sh
   - a shell script used for running the trace analysis tool on a single data object 
	 in the application with certain parameter setting. 
   - the parameter setting includes the initial memory address of the give data object
	 (INI_ADDR_ON_TDD), the error propagation threshold(ERR_PROP_THRESHOLD), the 
	 fault shadowing threshold(FAULT_MASK_THRESHOLD), the suffix for result files
	 (SERIAL_NUM), which usually consists of the application name and the name of 
	 given data object.

b. SerialRunning.sh
   - a shell script used for running the trace analysis tool for a given data object
	 with a couple of parameter settings.
   - make changes to the settings accordingly based on your own requirements.

c. tier3Runing.sh
   - a shell script used for recognizing and extracting the parameter settings from 
	 the fault-injection-result filename for the re-run of the trace analysis tool. 
	 Such that users don't re-input the parameters for the second run of the trace 
	 analysis tool when more than one paramenter setting are used in the first run 
	 of the trace analysis tool.
