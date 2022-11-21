# todo.md

A "todo list" format that supports [Markdown](https://www.markdownguide.org/), tagging, [ABCD analysis](https://en.wikipedia.org/wiki/Time_management#ABCD_analysis), collaboration. The format is designed to work seemlessly with any text editor:
  * Markdown editors ([Obsidian](https://obsidian.md/), [Roam Research](https://roamresearch.com/))
  * Text editors ([Notepad](https://apps.microsoft.com/store/detail/windows-notepad/9MSMLRH6LZF3?hl=en-us&gl=us), [TextEdit](https://support.apple.com/guide/textedit/welcome/mac), [VS Code](https://code.visualstudio.com/docs/languages/markdown))
  * Command line editors ([vim](https://www.vim.org/), [nano](https://www.nano-editor.org/), [micro](https://micro-editor.github.io/))

# Syntax
| Feature | Code |
| --- | --- |
| Incomplete Task | `* [ ] Call Saul` |
| Completed Task | `* [x] Call Saul` |
| Description | `* [ ] Call Saul: ask for help` |
| High Priority | `* [ ] (A) Call Saul` |
| Medium Priority | `* [ ] (B) Call Saul` |
| Low Priority | `* [ ] (C) Call Saul` |
| Cancel/ignore | `* [ ] ~~Call Saul~~` |
| Due Date | `* [ ] Call Saul 2009-04-26` |
| Tag(s) | `* [ ] Call Saul #work #backlog` |
| Assignee(s) | `* [ ] Call Saul @me @jesse` |

### Examples

```
* [ ] Go shopping #work @jesse
* [ ] ~~Pay Gretchen/Elliot #backlog~~
* [x] (B) Call Saul: ask for help 2009-04-29 #work #backlog @me @jesse
```

Here's that code rendered:
* [ ] Go shopping #work @jesse
* [ ] ~~Pay Gretchen/Elliot #backlog~~
* [x] (B) Call Saul: ask for help 2009-04-29 #work #backlog @me @jesse

---

## Grammar

```
     <word> ::= <ALNUM> | "-" | "_"
   <status> ::= "[ ]" | "[x]"
  <priority ::= "A" | "B" | "C"
     <tags> ::= "#"<word> [<tags>]
<assignees> ::= "@"<word> [<assignees>]
  <content> ::= ["("<priority>")"] <title>[":" <description>] [<date>] [<tags>] [<assignees>]
     <task> ::= "*" [<status>] (<content>|"~~"<content>"~~")
```

# See Also
* [Todo.txt](http://todotxt.org/)
* [todomd/todo.md](https://github.com/todomd/todo.md)
* [Wikipedia - Time Management](https://en.wikipedia.org/wiki/Time_management)
