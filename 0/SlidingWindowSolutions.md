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

# String anagrams

```Python
def find_string_anagrams(string, pattern):
	if len(string) < len(pattern):
		return []

	result = []
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
			result.append(i)

		if i >= len(pattern) - 1:
			leftChar = string[windowStart]
			windowStart += 1
			if leftChar in charFrequency:
				if charFrequency[leftChar] == 0:
					matched -= 1
				charFrequency[leftChar] += 1
	return result
```

# Smallest window containing substring



```Python
def find_substring(string, pattern):
  window_start, matched, substr_start = 0, 0, 0
  min_length = len(string) + 1
  char_frequency = {}

  for chr in pattern:
    if chr not in char_frequency:
      char_frequency[chr] = 0j
    char_frequency[chr] += 1

  for window_end in range(len(string)):
    right_char = string[window_end]
    if right_char in char_frequency:
      char_frequency[right_char] -= 1
      if char_frequency[right_char] >= 0:
		matched += 1

    while matched == len(pattern):
      if min_length > window_end - window_start + 1:
        min_length = window_end - window_start + 1
        substr_start = window_start

      left_char = string[window_start]
      window_start += 1
      if left_char in char_frequency:
		if char_frequency[left_char] == 0:
          matched -= 1
        char_frequency[left_char] += 1

  if min_length > len(string):
    return ""
  return str[substr_start:substr_start + min_length]
```
# Word concatenation

```Python
def find_word_concatenation(str, words):
  if len(words) == 0 or len(words[0]) == 0:
    return []

  word_frequency = {}

  for word in words:
    if word not in word_frequency:
      word_frequency[word] = 0
    word_frequency[word] += 1

  result_indices = []
  words_count = len(words)
  word_length = len(words[0])

  for i in range((len(str) - words_count * word_length)+1):
    words_seen = {}
    for j in range(0, words_count):
      next_word_index = i + j * word_length
      word = str[next_word_index: next_word_index + word_length]
      if word not in word_frequency: 
        break

      if word not in words_seen:
        words_seen[word] = 0
      words_seen[word] += 1

      if words_seen[word] > word_frequency.get(word, 0):
        break

      if j + 1 == words_count 
        result_indices.append(i)

  return result_indices
```
