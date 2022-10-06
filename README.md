# Prime numbers

A positive integer greater than 1 which has no other factors except 1 and the number itself is called a prime number. 2, 3, 5, 7 etc. are prime numbers as they do not have any other factors. But 6 is not prime (it is composite) since, 2 x 3 = 6.



## Using a flag variable (prime1.py)
In this program, we have checked if num is prime or not. Numbers less than or equal to 1 are not prime numbers. Hence, we only proceed if the num is greater than 1.

We check if num is exactly divisible by any number from 2 to num - 1. If we find a factor in that range, the number is not prime, so we set flag to True and break out of the loop.

Outside the loop, we check if flag is True or False.

If it is True, num is not a prime number.
If it is False, num is a prime number.


```python
num = float(input("Enter a number: "))

# prime numbers are greater than 1
if num > 1:
   # check for factors
   for i in range(2,num):
       if (num % i) == 0:
           print(num,"is not a prime number")
           print(i,"times",num//i,"is",num)
           break
   else:
       print(num,"is a prime number")
       
else:
   print(num,"is not a prime number")
```

## Using a for...else statement(Prime_Numbers.py)

Here, I have used a for..else statement to check if num is prime.

It works on the logic that the else clause of the for loop runs if and only if yiu don't break out the for loop. That condition is met only when no factors are found, which means that the given number is prime.

So, in the else clause, we print that the number is prime.


```python
num = float(input("Enter a number:"))
# If given number is greater than 1
if num > 1:
	# Iterate from 2 to n / 2
	for i in range(2, int(num/2)+1):
		# If num is divisible by any number between
		# 2 and n / 2, it is not prime
		if (num % i) == 0:
			print(num, "is not a prime number")
			break
	else:
		print(num, "is a prime number")
else:
	print(num, "is not a prime number")
```
## Links
[Programiz](https://www.programiz.com/python-programming/examples/prime-number)
