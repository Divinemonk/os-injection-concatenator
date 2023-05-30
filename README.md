# OS Injection Command Concatenator Cheatsheet

> Linux &amp; Windows special characters that can be use to concatenate system (terminal/commandline) commands


- goto [main table](#special-characters-w-os-specific-description)


<br>

# Use case
It's important to note that the use of special characters for command concatenation, as described earlier, is not directly related to OS injection vulnerabilities. OS injection vulnerabilities typically occur when untrusted input is passed to an operating system command without proper sanitization or validation.

However, in some cases, the improper handling of special characters can lead to OS injection vulnerabilities. If user-supplied input is concatenated directly into a command without proper validation or escaping, an attacker may be able to inject additional commands or manipulate the execution flow. This can be especially risky when user input is combined with special characters used for command concatenation.

<br>

## Special characters w/ os specific description

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

<br>
<hr>
<br>

## Prevent OS injection vulnerabilities
> It's important to follow secure coding practices

 1) __Input validation and sanitization__: Validate and sanitize all user input before using it in commands. This includes checking for malicious characters, removing or escaping special characters, and enforcing strict input formats.
 2) __Parameterized queries__: If you're executing database queries or interacting with external systems, use parameterized queries or prepared statements instead of concatenating user input directly into the command. This helps prevent injection attacks by automatically handling escaping and quoting.
 3) __Command whitelisting__: Maintain a whitelist of allowed commands or actions and validate user input against this whitelist. Only allow specific commands that are necessary for the application's intended functionality.
 4) __Least privilege principle__: Ensure that the commands or processes executed have the minimal necessary privileges. Avoid running commands with elevated privileges unless absolutely required.
 5) __Regular security updates__: Keep your operating system and software up to date with the latest security patches to protect against known vulnerabilities.
