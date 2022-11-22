# todo.md

A "todo list" format that supports [Markdown](https://www.markdownguide.org/), tagging, [ABCD analysis](https://en.wikipedia.org/wiki/Time_management#ABCD_analysis), collaboration. The format is designed to work seemlessly with any text editor:
  * Markdown editors ([Obsidian](https://obsidian.md/), [Roam Research](https://roamresearch.com/))
  * Text editors ([Notepad](https://apps.microsoft.com/store/detail/windows-notepad/9MSMLRH6LZF3?hl=en-us&gl=us), [TextEdit](https://support.apple.com/guide/textedit/welcome/mac), [VS Code](https://code.visualstudio.com/docs/languages/markdown))
  * Command line editors ([vim](https://www.vim.org/), [nano](https://www.nano-editor.org/), [micro](https://micro-editor.github.io/))

# Syntax
| Feature | Code |
| --- | --- |
| Incomplete task | `* [ ] Call Saul` |
| Complete a task | `* [x] Call Saul` |
| Description | `* [ ] Call Saul: inqiure about nephew's arrest` |
| High Priority | `* [ ] (A) Call Saul` |
| Medium Priority | `* [ ] (B) Call Saul` |
| Low Priority | `* [ ] (C) Call Saul` |
| Cancel/ignore a task | `* [ ] ~~Call Saul~~` |
| Tag(s) | `* [ ] Call Saul #work #backlog` |
| Due Date | `* [ ] Call Saul due:2009-04-26` |
| Assignee(s) | `* [ ] Call Saul @me @jpinkman` |

### Examples

```
* [ ] Go shopping #work @jpinkman
* [ ] ~~Pay Gretchen/Elliot: hospital bills~~ #backlog
* [x] (B) Call Saul: inquire about nephew's arrest #work #backlog due:2009-04-29 @me @jpinkman
```

Use your favorite markdown editor, edit/view the todo list:

### GitHub Flavored Markdown

---

* [ ] Go shopping #work @jpinkman
* [ ] ~~Pay Gretchen/Elliot: hospital bills~~ #backlog
* [x] (B) Call Saul: inquire about nephew's arrest #work #backlog due:2009-04-29 @me @jpinkman

---

### Obsidian
![obsidian](https://user-images.githubusercontent.com/48300131/203187819-b38ec602-c1bc-4c64-a729-c2d545a987f4.png)

## Grammar

```
     <word> ::= <ALNUM> | "-" | "_"
   <status> ::= "[ ]" | "[x]"
 <priority> ::= "A" | "B" | "C"
     <tags> ::= "#"<word> [<tags>]
<assignees> ::= "@"<word> [<assignees>]
  <content> ::= ["("<priority>") "]<TITLE>[": "<DESCRIPTION>]
     <meta> ::= [<tags>] ["due:"<DATE>] [<assignees>]
     <task> ::= "*" [<status>] (<content>|"~~"<content>"~~") [<meta>]
```

# See Also
* [Todo.txt](http://todotxt.org/)
* [todomd/todo.md](https://github.com/todomd/todo.md)
* [Wikipedia - Time Management](https://en.wikipedia.org/wiki/Time_management)
