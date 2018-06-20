This is basically just me writing down things I find myself searching how to do
in Vim often, or maybe some cool, obscure things I find.

Most of the text and tips is cribbed from the Vim wiki so far.

--------------------------------------------------------------------------------

Finding a whole word
--------------------
In a program, you may want to search for an identifier named `i`. However,
entering the search `/i` will find every hit, including the "i" in words like 
"if" and "while". In a pattern, `\<` represents the beginning of a word, and 
`\>` represents the end of a word, so to find only the whole word "i", use the
pattern:

```\<i\>```
[See here for more details][1]

Removing Whitespace
-------------------
In a search, `\s` finds whitespace (a space or a tab), and `\+` finds one or 
more occurrences.

The following command deletes any trailing whitespace at the end of each line.
If no trailing whitespace is found no change occurs, and the `e` flag means no
error is displayed.

```:%s/\s\+$//e```

The following deletes any leading whitespace at the beginning of each line.

```:%s/^\s\+//e```

[See here for more details][2]








[1]: http://vim.wikia.com/wiki/Search_patterns
[2]: http://vim.wikia.com/wiki/Remove_unwanted_spaces
