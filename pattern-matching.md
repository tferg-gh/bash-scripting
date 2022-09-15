# Pattern Matching

> Pattern matching is used in Bash for the [[ and case keywords, pathname expansion,
  and some types of parameter expansion.

	*	Matches any string, including null.

	?	Matches any single character.

	[character class]

		Matches any one of the characters enclosed between [ and ]

	> [^...] 

		matches the complement (any character not in the class)

	> [x-z] 

		matches the range of character from x to z

	> [[:class:]]

		matches according to these POSIX classes:

		alnum, alpha, ascii, blank, cntrl, digit, graph, lower, print, punct, space
