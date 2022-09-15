# Conditionals: case

case word in
	pattern1)
		list1;;
	pattern2 | pattern3)
		list2;;
esac

	Match word against each pattern sequentially. 

	When the first match is found, evaluate the list corresponding to that match
	and stop matching.

	> The | (pipe) character between two patterns entails a match if either
	  pattern matches (OR)

```
case one in
	o)
		echo 'o'
	;;
	o*)
		echo 'o*'
	;;
	*)
		echo 'nope'
	;;
esac
```
	> one is a string in this scenario not a variable

	> If we run this we're going to get the output of o*

	> This is because the match is not exhaustive 

	> You need to fully match the pattern

	> So while o is in one o* matches the letter o and any number of characters
	  afterwards.
