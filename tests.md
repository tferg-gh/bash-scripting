# Tests

## [ expression ] or test expression

	Evaluate conditional expression with the test builtin.

	This is the old way of doing it. This is either a builtin or a file command.

## [[ expression ]]

	Evaluate conditional expression with the [[ keyword. 
	
	Word splitting is not performed. 
	
	The righthand side of a string comparison (==. !=) is treated 
	as a pattern when not quoted and as a string when quoted.

	Pattern matching is not the same as regular expressions, it's similar to what
	you use in globbing. 

	E.g. *.txt 

	True if:

	> [[ -n string ]]
		string is non-empty

	> [[ -z string ]] 	
		string is empty

	> [[ string1 == string2 ]]
		string1 and string2 are the same

	> [[ string1 != string2 ]]
		string1 and string2 are not the same

	> [[ string =~ regex ]]
		string matches regular expression

		> When you match with a regular expression, the parts that you 
		  match get pulled out into an array, so you can do back references
		  that way too.

	> [[ -e file ]] 
		file exists

	> [[ -f file ]]
		file is a regular file

	> [[ -d file ]]
		file is a directory

	> [[ -t fd ]]
		fd is open and refers to a terminal

		> This tells us that the input that we're working with it coming from
		  a terminal. i.e. if a user is inputing the command or if it's from an
		  automated process. 

		```
		[ -t 0 ] # will return successfull as 0 = stdin
		[ -t 0 ] < /etc/os-release # will return non-zero as it's isn't stdin
		```

