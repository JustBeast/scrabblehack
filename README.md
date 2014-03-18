scrabblehack
============
f = open("words", "r")

letters= raw_input("Enter your rack: ")
letters.upper()
scores = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2,
         "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3,
         "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1,
         "r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4,
         "x": 8, "z": 10}

perms = [''.join(p) for p in itertools.permutations(letters)]
sowpods= f.readlines()
x = []
for perm in perms:
	if perm in sowpods:
		x.append(perm)
s=0
for b in x:
	letters = list(b)
	for letter in letters:
		s+=scores[letter.lower]
#this breaks up the letters of a word and then finds its score
sum(s)




#will s equal the total of the scores of all the words







