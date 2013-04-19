# Python Single Line Converter

See <http://jagt.github.io/python-single-line-convert/>

Convert multiple line Python code to a single line in a dead simple way.

## Rationale

Ease copy pasting Python code in some cases (e.g paste into Python shell or through Putty). If you find yourself need this a lot you may consider using [ipython](http://ipython.org/) with the `%paste` command, or a graphic based one like [dreampie](http://www.dreampie.org/)

## How it works

Basically it paste your multiline code together into a triple quoted string and wraps it with [exec](http://docs.python.org/2/reference/simple_stmts.html#the-exec-statement). To keep the code legal the string is processed as follows:

1. Escape all `\`, then escape `"""`.
2. Reindent to 0 indent based on first line if option is selected. So you can paste indented code directly.
3. Wraps `exec` statement or function based on version option.

## Limitations

1. Won't remove comments and docstring. Properly handling these needs more work.
2. Of course can't check the original code is syntatically legal or properly indented.
3. Only tested by randomly copying code from Python Recipes... So please report missing cases.

