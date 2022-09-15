# Brace Expansion

Arbitrary Word Generation

## String generation
	
	prefix{ab,cd,ef}suffix
	
	```
	$ echo bash{,e{d,s},ful{,ly,ness},ing}
	bash bashed bashes bashful bashfully bashfulness bashing
	```

	> An empty brace in your expansion won't add anything new but will add the word

	```
	$ man man
	$ man{,}
	```

	> These are the same thing

## Sequence generation

	prefix{x..y}suffix

## Sequencing by specified increment

	prefix{x..y..incr}suffix

	```
	$ echo [10..55..5]%
	10% 15% 20% 25% 30% 35% 40% 45% 50% 55%
	```

> Brace expansion may be nested and combined

> The prefix and suffix are optional
