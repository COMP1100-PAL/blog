## Activity

For any of the extensions we want to complete the following tasks, in order to gain a good understanding both the compression concept and how to code it. 

1. Complete an example of encoding a message. You may use the message, "Antony Hosking", as an example.
2. Complete an example of decoding the same message.
3. Write down the steps you took for each of these processes.
4. Write down the type of the data at each step in this process. e.g. starts as a `String`, then become a `[String]`, then becomes etc.
5. Write out function signatures, for a number of functions which we will use in encoding and decoding.
6. Identify how these 'helper funcions relate to eachother.
7. Ask a mentor if you got it all correct.
8. Go back to your computers and code the functions (this part will be private).

## RLE

If you're finished huffman encoding then this task is actually considerably easier. Rather than leading you through this one we will simply point you toward three useful function `group`, `length` and `head`. `group` can take a string and returns a list of Strings of the homogenous elements. i.e. `group "aaabbbcccaa" = ["aaa","bbb","ccc","aa"]`. `length` simply finds the length of a list. `head` takes the first element from a list.

To decode RLE a useful function might be `repeat`.

## BWT

In my personal opinion, coding BWT is easier than understanding how it works. 

To begin with we need to generate all the rotations of a string. We then sort this list, using any sorting method we had before. We can then use `last` on each string now, to find the encoding. 

Decoding is another problem entirely. In haskell we don't have loops, so we need to use recursion. We can similate the repeating part in haskell using a helper function. We will simply reference the wikipedia entry for this `https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform`. 

1. Try to apply BWT to `ANTONY HOSKING`.
2. Break up the algorithm into a number of functions which we need to write. 
3. Write the functions.

## MTF

To begin with the encoding the string, we start with a list representing our dictionary. Each time we encode a letter of our string we need to change our dictionary, by moving the letter to the front of the dictionary. We encode the letter as the index of the string within the dictionary. `elemIndex` may be a useful function to do this. 

Decoding using MTF is quite easy though. You can use the `!!` function to find the element in a list at a particular index. 

1. Try to apply BWT to `ANTONY HOSKING`.
2. Break up the algorithm into a number of functions which we need to write. 
3. Write the functions.

## Prefix Tree


