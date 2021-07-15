## Qn.1 Compose a program that creates a one-dimensional array a containing exactly 1000 integers, and then attempts to access a[1000]. What happens when you run the program?

	a) 1000
	b) Value of the arrray at the start
	c) value of the array at the end
	d) indexing error

	ANS. 
		D: Indexing error


## Qn.2 What is wrong with the following code fragment?

		a = []
		for i in range(10):
		    a[i] = i * i

	ANS. 
		Running this code throws an IndexError: list assignment index out of range, this is because a is an empty array hence we don't have any elements appended to the array and therefore attempting to use them in the assignment statement we get an IndexError.
	 	


## Qn.3 What does the following code fragment write?

		a = stdarray.create1D(10, 0)
		for i in range(10):
		   a[i] = 9 - i
		for i in range(10):
		   a[i] = a[a[i]]
		for v in a:
		   stdio.writeln(v)


	ANS.


## Qn.4 What is a[] after executing the following code fragment?

		n = 10
		a = [0, 1]
		for i in range(2, n):
		    a += [a[i-1] + a[i-2]]
		    print (a)

	ANS.

		[0, 1, 1]
		[0, 1, 1, 2]
		[0, 1, 1, 2, 3]
		[0, 1, 1, 2, 3, 5]
		[0, 1, 1, 2, 3, 5, 8]
		[0, 1, 1, 2, 3, 5, 8, 13]
		[0, 1, 1, 2, 3, 5, 8, 13, 21]
		[0, 1, 1, 2, 3, 5, 8, 13, 21, 34]


## Bonus. Compose a program that takes an integer command-line argument n and writes n poker hands (five cards each) from a shuffled deck, separated by blank lines.


	ANS. 

		import random

		suits = ["Hearts", "Spades", "Clubs", "Diamonds"]
		ranks = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Jack", "Queen", "King", "Ace"]
		deck = []

		for suit in suits:
		    for rank in ranks:
		        deck.append(f'{rank} of {suit}')

		print (f'There are {len(deck)} cards in the deck.')
		print ()
		print ("Dealing........")
		print()

		player_1 = []
		player_2 = []

		while len(player_1)<5:
		    card = random.choice (deck)
		    deck.remove (card)
		    player_1.append(card)
		    card_2 = random.choice(deck)
		    deck.remove(card_2)
		    player_2.append(card_2)

		print (f'There are now {len(deck)} cards in the deck.')
		print ()
		print ("Player1 has the following cards in their hand: ")
		print (player_1)
		print ()
		print ("Player2 has the following cards in their hand: ")
		print (player_2)
		print ()


