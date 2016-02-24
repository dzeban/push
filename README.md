push - Python Uber Shell
========================

"Hate" is the strong word but I really don't like bash.

`push` provides common shell utilities such as command execution with the power
and readability of Python. It's a shell with Python as THE language.

Here is the quick example:

    bash$ ./push 
    [[[ ::: Python Uber Shell ::: ]]]
    $ ls /
    bin   dev  home  lib64       media  opt   root  sbin  sys  usr
    boot  etc  lib   lost+found  mnt    proc  run   srv   tmp  var
    $ cat /etc/issue
    \S
    Kernel \r on an \m (\l)

    $ # Comments are here, don't worry
    $
    $ # Here is how we catch errors from commands
    $ ls /invalid
    ls: cannot access /invalid: No such file or directory
    ls returned 2, error: None
    $ 
    $ # Now the python!
    $ a = 2
    $ print(a)
    2
    $ a += 2
    $ print(a)
    4
    $ # It's not only variables, but functions and loops and stuff!
    $ def show33(val): print(val + 33)
    $ show33(10)
    43
    $ for i in range(3): show33(i)
    33
    34
    35
    $
    $ import this
    The Zen of Python, by Tim Peters

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!
    $
    $ # Here's how we handle python errors
    $ show33('abc')
    Python evaluation error: <class 'TypeError'>
    push: show33('abc'): no such command

`push`'s ultimate goal is to replace bash as the default shell in most unix distros.
