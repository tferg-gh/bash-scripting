# Condtionals: if

if list1; then list2; fi

	Evaluate list1, then evaluate list2 only is list1 returns a status of 0.

if list1; then list2; else list3; fi

	Evaluate list1, then evaluate list2 only if list1 returns a status of 0.
	Otherwise, evaluate list3.

if list1; then list2; elif list3; then list4; else list5; fi

	Evaluate list1, then evaluate list2 only if list1 returns a status of 0.
	Otherwise, evaluate list3, then evaluate list4 only if list 3 returns a 
	status of 0. Otherwise, evaluate list5.

> You can put as many elif's (or elseif) as you want in the middle

```
if [ "a" == "a" ]
then
	echo "yep"
else
	echo "nope"
fi
```
