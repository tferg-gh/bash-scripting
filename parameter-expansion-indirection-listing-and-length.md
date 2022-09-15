# Parameter Expansion: Indirection, Listing, and Length

				param="parade"; parade="long"; name=( gnu not unix )

## Indirect expansion

${!param}			long

## List names matching prefix "pa"

${!pa*} or "${!pa@}"		parade param

## List keys in array

${!name[*]} or "${!name[@]}"	0 1 2

## Expand to length

${#param} 			6
