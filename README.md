# grop / egrop

I use these two scripts for having to type less when using [gron](https://github.com/tomnomnom/gron).

The usual workflow for gron is `cat example.json | gron | grep <something> | gron -u`.

`grop` combines the gron, grep and ungron steps. Therefore, `grop` is a portmanteau of gron and grep.

## grop
`grop` is a shorthand for my 80% use case where I just want to grep for one or more keywords:

`grop foo bar baz`\
is equivalent to\
`gron | grep "foo|bar|baz" | gron -u`\

## egrop
`egrop` is a shorthand for the other 20% where I want to pass some other flags to grep. `egrop` will just forward its arguments to grep:

`grop -i -v address`\
is equivalent to\
`gron | grep -i -v address | gron -u`\
