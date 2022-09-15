# Functions

Functions are compound commands which are defined 
in the curent shell and given a function name, which
can be called like other commands.

func.name () compound_cmd

	Assign compound_cmd as function name func.name

func.name () compound_cmd [>,<,>>] file

	Assign compound_cmd as function named func.name;
	function will always redirect to (>), from (<), or append
	to (>>) the specified file. Multiple file descriptors may 
	be specified, for instance: >out.file 2>err.log
