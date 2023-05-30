# OS Injection Concatenator 

> Linux &amp; Windows special characters that can be use to concatenate system (terminal/commandline) commands

<br>

| Special Character |	Usage in Linux | Usage in Windows |
|---|---|---|
|`;`|	Executes multiple commands sequentially |	Executes multiple commands sequentially|
|`&&`|	Executes the next command if the previous one succeeds | Executes the next command if the previous one succeeds|
|`\|\|`|	Executes the next command if the previous one fails |	Executes the next command if the previous one fails|
|`&`| Executes a command in the background |	Executes a command in the background|
|`>`|	Redirects output to a file | Redirects output to a file|
|`>>`|	Appends output to a file |	Appends output to a file|
|`<`|	Redirects input from a file |	Redirects input from a file|
|`2>`|	Redirects error output to a file |	Redirects error output to a file|
|`2>>`|	Appends error output to a file |	Appends error output to a file|
|`&>`|	Redirects both output and error output to a file |	Redirects both output and error output to a file|
|`&&`|	Uses conditional execution; executes the next command if the previous one succeeds|Uses conditional execution; executes the next command if the previous one succeeds|
