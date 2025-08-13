## Using claude

Taken from this video:

https://www.youtube.com/watch?v=AXz6TMAwqnY

Clearing context:

``
/clear
``

Compacting context

``
/compact 
``

or 

``
/compact <some text for new context>
``

Swich between modes:

``
shift-tab
``

For example you can use shift-tab to move into plan mode

Modes:

```
auto-accept edits
plan
```

You can set up permissions in this file:

``
.claude/settings-local.json
``
Contents:

```
{
  permissions: {
    "defaultMode": "acceptEdits",
    "allow": {
      "Bash: [npm init: *]",
      "Bash: [tsx: *]",
      "Bash: [npm: test:*]"
    }
    "deny": []
  }
}
```

Using hash command on claude prompt.  If you add the hash followed by an instruction, it will add it to the context claude.md file.

Using ! followed by commad.  It will execute what ever command you typed after the exclamation.  It will add it to the context.

You can type on the prompt:

- think
- think hard
- think harder
- ultrathink

This allows you to control how many tokens it uses to solve a problem.

Bring command back:

``
ctrl + -
``

You can take a screenshot and type:

``
ctrl v
``

and it will type:

``
[Image #1]
``

You can type a question:

``
[Image #] What is this
``

You can add additional directories to the context when starting claude:

``
claude --add-dir ../apps ../lib
``

Or you can just add it on the command line:

``
/add-dir </path-to-directory>
``

Asking a quick question:

``
claude -p "What does the code do"
``

Go back to a specific conversation with claude:

``
claude --resume
``

It will show you a summary of all your previous conversations and you can choose one.

In the md files you can add keywords like:

'''
MUST
MUST NOT
'''
