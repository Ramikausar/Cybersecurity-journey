Cryptography Fundamentals
Overview

Cryptography is the practice of securing information by transforming readable data (plaintext) into an unreadable format (ciphertext). It helps achieve confidentiality, integrity, authentication, and non-repudiation in information systems.

This repository demonstrates several classical cryptographic algorithms:

Caesar Cipher
Playfair Cipher
Rail Fence Cipher
Row Transposition Cipher


1. Caesar Cipher

Description

The Caesar Cipher is a monoalphabetic substitution cipher in which each letter of the plaintext is shifted by a fixed number of positions in the alphabet.

Encryption:-
    C=(P+K)mod26

Decryption:-
    P=(C−K)mod26

Where:-
    P = Plaintext character
    C = Ciphertext character    
    K = Shift key
    mod 26 = Number of letters in English alphabe

    Plaintext:

Example:-
    Plaintext : HELLO
    Key : 3
    Ciphertext : KHOOR

Explanation:-
    Plain Letter	        Shift +3	        Cipher Letter
        H	             H → I → J → K	              K
        E	             E → F → G → H	              H
        L	             L → M → N → O	              O
        L	             L → M → N → O	              O
        O	             O → P → Q → R	              R

THE SAME WAY IT WILL Decrypt FROM KHOOR TO HELLO


2. Playfair Cipher

Description

The Playfair Cipher encrypts pairs of characters rather than individual letters. It uses a 5×5 matrix generated from a keyword.

THIS CIPHER HAVE THREE  Encryption  RULES 

    .Same Row
        Replace each letter with the letter immediately to its right.
    
    .Same Column
        Replace each letter with the letter immediately below it.
    
    .Rectangle Rule
        Replace each letter with the character located at the opposite corner of the rectangle.


Keyword : KINGS

Step 1: 
        Create 5×5 Matrix
        Remove duplicate letters from the keyword and fill remaining alphabet letters.

        (I and J share one position)
        Because a 5×5 matrix contains only 25 cells while the English alphabet has 26 letters, I and J are usually combined.

				
                            K	I	N	G	S
                            A	B	C	D	E
                            F	H	J	L	M
                            O	P	Q	R	T
                            U	V	W	X	Y

Step 2: 
        Plaintext  :  KAUSAR

        Split into pairs:
                    KA  US  AR


Encrypt Pair 1: KA

        Locate letters:
                K → Row 1, Column 1
                A → Row 2, Column 1
        Both are in the same column.

        Rule: If letters are in the same column, replace each with the letter below it.
                K → A
                A → F
        Result:
                KA → AF

Encrypt Pair 2: US
        Locate letters:
                U → Row 5, Column 1
                S → Row 1, Column 5

        They form a rectangle.
        Rule: Replace each letter with the letter in the same row but at the other corner of the rectangle.
                U → Y
                S → K
        Result:
                US → YK

Encrypt Pair 3: AR

        Locate letters:
                A → Row 2, Column 1
                R → Row 4, Column 4
        They form a rectangle.

        Rule: Take opposite corners.
                A → D
                R → O
        Result:
                AR → DO

Final Ciphertext

        Combine all encrypted pairs:
                AF + YK + DO

        Ciphertext
                AFYKDO
        
Decryption Verification

        Ciphertext:
                AFYKDO

        Split into pairs:
                AF  YK  DO

        Apply reverse Playfair rules:

                AF → KA
                YK → US
                DO → AR

Recovered Plaintext:
        KAUSAR

3. Rail Fence Cipher

Description

Rail Fence Cipher is a transposition cipher in which plaintext letters are written in a zigzag pattern across rails and then read row by row.

Example
    Plaintext : HELLOWORLD
    Rails : 3

Step 1 : Write Zigzag
         
         Rail 1: H  O   L
         
         Rail 2:  E L W R D
         
         Rail 3:   L   O

Visual Pattern:

  H      O      L
    E   L  W  R   D
      L     O

Read Row by Row

Rail 1:
    HOL
Rail 2:
    ELWRD
Rail 3:
    LO

Combine:
    HOLELWRDLO

How Decryption Works
        Draw zigzag pattern.
        Count spaces.
        Fill ciphertext letters row-wise.
        Read zigzag path.

        HELLOWORLD


4. Row Transposition Cipher

Description 
Row Transposition Cipher rearranges characters according to a numerical key.
Characters are written row-wise and read column-wise based on key order.

Example :
    Plaintext
        KAUSARRAMI
    Key
        3421

Step 1 : Create Table
    3	4	2	1
    K	A	U	S
    A	R	R	A
    M	I	X	X


Step 2 : Arrange Key
    Key:
        3 4 2 1
    Ascending order:
        1 2 3 4
    Corresponding columns:
        4 3 1 2

Step 3 : Read Columns

    Column 4:
        SAX
    Column 3:
        URX
    Column 1:
        KAM
    Column 2:
        ARI

Ciphertext
    SAXURXKAMARI


Quick Comparison

    Cipher                          Type                       Key

Caesar Cipher                   Substitution                Shift Number
Playfair Cipher                 Digraph Substitution        Keyword
Rail Fence Cipher               Transposition               Number of Rails
Row Transposition Cipher        Transposition               Numeric Key


Key Difference
    - Caesar Cipher changes letters.
    - Playfair Cipher changes pairs of letters.
    - Rail Fence Cipher changes positions.
    - Row Transposition Cipher rearranges columns.