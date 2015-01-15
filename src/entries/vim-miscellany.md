title: vim miscellany
created: January 14, 2015
blurb: random recent vim learnings
tags:
    - vim

---

some vim tips that I've picked up recently

* find and replace within a selection:
  * select a block visually
  * type : to start entering a command
  * s/red/green/g to change all reds to greens
  * this was a bit confusing as non-visual mode selection is the same command but with a percent sign :/
 
* find/replace a word under the cursor
as per [this article](http://vim.wikia.com/wiki/Search_and_replace_the_word_under_the_cursor)
  * type *
  * ciw (change inner word)
  * `<esc>`
  * then n (next occurrence)
  * and . (repeat change)

* I've been building little go scripts in vim and this pops up the quickfix pane when there's an error
  * my vimrc has two ways of hiding this: call ToggleErrors() and :ccl

* opening ctrlp selections in a split:
  * with the file highlighted, type ctrl-x to open in a horizontal split
  * ctrl-v opens in a vertical split
  * I still almost always create the split first

* I keep forgetting I have easy-motion
  * jump to the letter d, anywhere:
  * <leader>ssd

* I should learn snippets..

