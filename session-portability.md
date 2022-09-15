# Session Portability

Import elements from current session directly into a new local or remote session.

sudo bash -c "$(declare -p parameters; declare -f functions) code and stuff"

	Import parameters and functions into root shell, then run code and stuff

	```
	sudo bash -c "$(declare -f memtop); memtop"
	```

	> This will take the function that is declared in my current shell session
	  and interpolate the whole definition and then run it as root
	  

ssh remote_host "$(declare -p parameters; declare -f functions) code and stuff"

	Import parameters and functions into remote shell, then run code and stuff

	> declare can list parameters and functions from the current shell, or can 
	  set parameter attributes.

	> When sourcing or interpolating Bash code, be mindful of shell options
	  which affect parsing, such as extglob, if the code relies on that syntax

	> declare -f for functions

	> decalre -p for parameters, arrays or variables
