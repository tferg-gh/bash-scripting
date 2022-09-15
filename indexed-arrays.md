# Indexed Arrays


## Assign an array by elements

	array=(zero one two "three and more")

	```
	$ declare -p array
	declare -a array=([0]="zero" [1]="one" [2]="two" [3]="three and more")
	```

## Add an element to an array

	array+=("four and beyond")

	```
	declare -p array
	declare -a array=([0]="zero" [1]="one" [2]="two" [3]="three and more" [4]="four and beyond")
	```

## Recreate array with spaces in elements as underscores

	array=("${array[@]// /_}")

	```
	declare -p array
	declare -a array=([0]="zero" [1]="one" [2]="two" [3]="three_and_more" [4]="four_and_beyond")
	```

## Recreate array only with elements from index 2 to 4

	array=("${array[@]:2:3}")

	```
	declare -p array
	declare -a array=([0]="two" [1]="three_and_more" [2]="four_and_beyond"
	```

## Print element at index 1 of array

	echo "${array[1]}"

	```
	three_and_more
	```

## Print array indexes

	echo ${!array[@]}

	```
	0 1 2
	```

	> Associative arrays are available in Bash 4 and greater
	  Which means instead of having an index you can have key value pairs, like a simple
	  perl hash.
