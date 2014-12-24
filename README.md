This syntax file displays unicode characters for some Scala operators and
built-in functions, turning the following:

```scala
  foo =>
  foo <- bar
  foo -> bar
  2 <= 5
  5 >= 2
  2 == 2
  2 === 2l
  2 != 3
  2 =/= 2l
  foo && bar
  foo || bar
  foo map bar
  foo flatMap bar
```

into

```scala
  foo ⇒
  foo ← bar
  foo → bar
  2 ≤ 5
  5 ≥ 2
  2 ≟ 2
  2 ≡ 2l
  2 ≠ 3
  2 ≢ 2l
  foo ∧ bar
  foo ∨ bar
  foo ∘ bar
  foo ⤜ bar
```


Screenshot:

<img src="https://raw.github.com/mpollmeier/vim-scalaConceal/master/screenshot.png" title="Screenshot" />

*This does not – at any point – alter your source code*. It simply uses Vim's
"conceal" feature to “hide” `map` behind `∘`, etc. Whenever the cursor is at
a line with concealed text, the text will be expanded.

To install, simply put `scala.vim` in `~/.vim/after/syntax` or use something
like [Pathogen](https://github.com/tpope/vim-pathogen) (recommended).

Vim ≥ 7.3 is required.

This plug-in is very much inspired by
<https://github.com/ehamberg/vim-cute-python>
and
<http://github.com/Twinside/vim-haskellConceal>


