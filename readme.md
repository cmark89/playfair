This Python module allows the user to easily encrypt and decrypt messages using the Playfair method of ciphering plaintext.  It is simple to use.  First, import the module:

    import playfair

Next, you need to create the square that will be used for encoding:

    square = playfair.PlayfairSquare("KEYWORD")

Pass your desired keyword into the constructor of the PlayfairSquare.  This will initialize the translation table and prepare the square for ciphering.  Next, just call the PlayfairSquare.encrypt(string) and PlayfairSquare.decrypt(string) methods to your heart's content.

    print(square.encrypt("This is a secret message for the resistance!"))

The last thing you need to know about is the modes for translation.  There are two modes for translating a plaintext input into digraphs: one removes the letter Q from the message; the other instead replaces all instances of J with I.  The PlayfairSquare class defaults to using the Q-less mode, but you can optionally pass in a mode to use in the constructor of the square.

    square = playfair.PlayfairSquare("KEYWORD", playfair.MODE_IJSWAP)

The two modes and their constant names are MODE_NOQ and MODE_IJSWAP.

Now enjoy using the Playfair cipher faster than ever!
