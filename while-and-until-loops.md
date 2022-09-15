# While and Until Loops

*(Typically) iterate based on an external resource* which means at runtime we 
don't know how many iterations we're going to have. 

**while** list1; **do** list2; **done**

	Execute list1; if success, execute list2 and repeat. 
	
	Continue until list1 returns a non-zero status (fails).

	```
	while read var1 var2
	do
		echo $var2 $var1
	done
	```

	> read is successful as long as it read a line

	> the last variable will absorb any additional arguments 

	> you can avoid this by defining an unused variable last

	```
	while read var1 var2 var3
	do
		echo $var2 $var1
	done
	```

**until** list1; **do** list2; **done**

	Execute list1; if failure, execute list2 and repeat. 

	Continue until list1 returns a status of 0 (succeeds).

> Typically handy for processing lines of text: **while** **read**
