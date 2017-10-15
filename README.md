# jison2json \[SECONDARY SOURCE REPO]


[![build status](https://secure.travis-ci.org/GerHobbelt/jison2json.png)](http://travis-ci.org/GerHobbelt/jison2json)


[jison](http://jison.org) grammars come in two formats: JSON or a special text format similar to Bison's. This utility converts from the jison's format to JSON. See the [json2jison](https://github.com/zaach/json2jison) for the reverse conversion.


> 
> # deprecation ~ secondary-source notice
>
> From today (2017/oct/15) the jison2json repository is only a **secondary source** 
> for the `jison2json` package/codebase: the **primary source** is the 
> [jison](https://github.com/GerHobbelt/jison) 
> [monorepo](https://medium.com/netscape/the-case-for-monorepos-907c1361708a)'s `packages/jison2json/` 
> directory.
>
> (For a comparable argument, see also ["Why is Babel a monorepo?"](https://github.com/babel/babel/blob/master/doc/design/monorepo.md))
>
> Issues, pull requests, etc. for `jison2json` should be filed there; hence 
> we do not accept issue reports in this secondary repository any more.
>
> This repository will track the primary source for a while still, but be 
> *very aware* that this particular repository will always be lagging behind!
>



## install

    npm install @gerhobbelt/jison2json -g


## usage

    # single grammar
    jison2json grammar.y

    # or separate grammars
    jison2json grammar.y lex.l

Or require it and convert programatically:

    var jison2json = require('@gerhobbelt/jison2json');
    var grammar = "%% foo: bar { return true; };";

    var json = jison2json.convert(grammar);


## license

MIT
