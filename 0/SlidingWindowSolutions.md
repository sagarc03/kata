# Permutation in a String

```Python
def find_permutation(string, pattern):
	if len(string) < len(pattern):
		return False
	
	windowStart, found = 0, 0
	charsFrequency = {}

	for char in pattern
		if char not in charFrequency:
			charsFrequency[char] = 0
		charsFrequency += 1
	
	for i in range(len(string)):
		currentChar = string[i]
		if currentChar in charFrequency:
			charFrequency -= 1
			if charFrequency[currentChar] == 0:
				found += 1

		if matched == len(charFrequency):
			return True

		if i >= len(pattern) - 1:
			leftChar = string[windowStart]
			windowStart += 1
			if leftChar in charFrequency:
				if charFrequency[leftChar] == 0:
					matched -= 1
				charFrequency[leftChar] += 1
	return False
```
