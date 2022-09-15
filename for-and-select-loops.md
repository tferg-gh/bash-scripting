# For and Select Loops

*Iterate based on command line arguments* 

for name in words; do list; done

	During each iteration, assign name the value of the next word, then

	execute list. Repeat until all words have been exhausted.

	```
	for i in one two "three four"
	do
		echo "-.-.-$i-.-.-"
	done

	-.-.-one-.-.-
	-.-.-two-.-.-
	-.-.-three four-.-.-
	```
	> Notice how the quotations "" make three and four into one word.

for (( expr1 ; expr2 ; expr3 )); do list; done

	Evaluate expr1 (initialization), then loop over list of commands until 

	expr2 (condition) returns non-zero status (fails). After each iteration,

	evaluate expr3 (afterthought). The expressions are evaluated as 

	Arithmetic expressions.

	```
	for (( i=0 ; i<5 ; i++ ))
	do
		echo $i
	done
	```
	
	> This is the C style for loop. The initializer gets run to set the 
	  variable, the condition gets checked each time before the loop to 
	  see if it is successful, then the afterthought gets applied before
	  starting again. 

select name in words; do list; done

	Create a menu item for each word. Each time the user makes a selection

	from the menu, name is assigned the value of the selected word, and 

	REPLY is assigned the index number of the selection. 

	```
	select choice in one two "three four"
	do 
		echo "$REPLY : $choice"
	done
	```
