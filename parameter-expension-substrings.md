# Parameter Expansion: Substrings

				param="racecar"

## Extraction			
				offset of 3, length of 2

	${param:offset}		ecar

	${param:offset:length}	ec

	> Offset means start counting from this character

	> Length is how many characters to return 

## Removal from left edge

				Pattern is '*c'

	${param#pattern}	ecar

	${param##pattern}	ar

	```
	echo ${PATH}
	/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin

	echo ${PATH#*:}
	/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
	```

	> This removes everything before the first : colon character from the left

	```
	echo ${PATH##*:}
	/snap/bin
	```

	> This is considered greedy since it will remove everything until after the last colon


## Removal from right edge
				Pattern is 'c*'

	${param%pattern}	race

	${param%%pattern}	ra

	```
	echo ${PATH%:*}
	/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
	```

	> This removes everything before the first : colon character from the right
