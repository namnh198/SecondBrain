---
title: Bash (Unix Shell)
tags:
  - Linux
  - MacOS
published: true
createDate: 2024-08-20
---

Bash command are mainly supported MacOS, Linux. On Windows, you can use WSL, it's easy to setup and can use full-featured.

**Note:** [[Terminal ZSH]]
## Tools
- Apps: We have many applications such as cmder (Windows), iTerm2 (MacOs),... For me only, I usually WezTerm on MacOS and Linux
- Online: [repl.it](https://repl.it/languages/bash)
## Hotkeys
- `Ctrl` + `C`: interrupt current tasks
- `Ctrl` + `L`: clear the screen
- `Tab`: Autocomplete the commands / directories / file names / ...
- `Ctrl` + `Shift` + `V`: pastes from clipboard.
- For a long list: `Enter` to continue read, `q` to quit
- `Ctrl` + `A`: Move cursor to beginning of the line
## Multiple commands
```bash
# run at once 
command_1 && command_2
```
## `.sh` file
> [!note+] `#!/bin/bash` tells your terminal to run the script with `bash`. There are also `zsh`, `sh`, `fish`,...


> [!multi-column]
>
>> [!note]
>>  ```bash
>>  #!/bin/sh 
>>  echo 'some info' 
>>  command_1 
>>  command_2 
>>  # and then sh file.sh
>> ```
>
>> [!note]
>> ```bash frame="none"
>> # with arguments 
>> $file1 = $1 
>> wc $file1 # word count 
>> 
>> # multiple input args 
>> for FILE1 in "$@"; do 
>> 	wc $FILE1 
>> done
>> ```
