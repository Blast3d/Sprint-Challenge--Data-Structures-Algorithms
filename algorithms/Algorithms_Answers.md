Add your answers to the Algorithms exercises here.

****EXERCISE 1****
a: O(1)

b: O(n)

c: O(n^2)

d: O(1)

e: O(n^2)

f: O(n)

g: O(n)

**EXERCISE 2**
a: 

def max_index_diff(a, n):
	max_diff = -1
	for i in range(0, n):
		j = n - 1
		while(j > i):
			if a[j] > a[i] and max_diff < (j - i):
				max_diff = j - i
			j -= 1
	
	return max_diff

a = [20, 2, 9, 4, 11, 6, 5, 18, 1]
n = len(a)
max_diff = max_index_diff(a, n)
print(max_diff)

b: 
def broken_egg_checker(f, n):
  broke = False
  check = n/2
  while not broke:
    if(check >= f):
      broke = True
      print("broke on floor" + str(check))
    else:
      check += 1
  while broke:
    print("broke on floor" + str(check))
    check -= 1
    if(check < f):
      print('did not break on ' + str(check))
      broke = False
      check += 1
  print("the f floor is " + str(check))
***Exercise III.***