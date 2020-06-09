Shell
----

An opinionated shell command execution library written in ruby.

### Why Shell?

While scripting shell commands in ruby, you have multiple ways at
your disposal. You can use `\``, `system` etc to fire commands.

After executing a shell command, I often want to make multiple decisions
based on the recent execution, like whether to exit the program or
continue, whether to log some error or warning message to the user,
whether to show command output to the user etc. This library aims at
solving just that; by providing an abstraction on top of ruby standard
library.

### Usage

```
$irb> shell = Shell.new
$irb> shell.fire("ls")
$irb> shell.success? # true
```

### Up Next

1. Fire a shell command and return its exit code
2. Set errors when failure
3. Implement pre and post execution hooks
