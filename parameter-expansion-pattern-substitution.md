# Parameter Expansion: Pattern Substitution

					param="racecar"

## Substitution
					pattern is 'c?', string is 'T'

${param/pattern/string}			raTcar

	Replace one match

${param//pattern/string}		raTTar

	Greedy, replace as many matches as you can. 

## Substitute at left edge
					pattern is 'r', string is 'T'

${param/#pattern/string}		Tacecar

## Substitute at right edge

${param/%pattern/string}		racecaT


	> Note these are not regular expressions, they're patterns
