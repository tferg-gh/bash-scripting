# Parameter Expansion: Conditionals
> (check if variable is unset, empty, or non-empty)

			unset param	param=""	param="gnu"

${param-default}	default		-		gnu

${param=default}	name=default	-		gnu

${param+alternate}	-		alternate	alternate

${param?error}		error		-		gnu

Treat empty as unset

${param:-default}	default		default		gnu

${param:=default}	name=default	name-default	gnu

${param:+alternate}	-		-		alternate

${param:?error}		error		error		gnu

> These are in POSIX so they can be run in sh as well as bash

> Allows you to specify default values

> Allows you to error out on certain things

> Alternate is interesting because when the value is defined we return something else

```
param="" 		# set the value of param to empty
echo ${param} 		# this will echo a new line
echo ${param:-default}	# this will echo default because the parameter is empty
echo ${param:-$HOME} 	# this will echo the users home directory
```

> This will not change the value of the parameter

```
echo ${param:=$HOME} 	# this will echo the users home directory and change the value of param
```

> The colon : treats emptiness as if the parameter is unset 
