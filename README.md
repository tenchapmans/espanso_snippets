# espanso_snippets
place to store the espanso yml files I use.   

Some pulled from other git repos

https://github.com/Lissy93/espanso-config

https://github.com/ekiel/espanso/blob/master/default.yml

Notes
The key is to use symbolic links, which are available in all operating systems. The idea is to move your espanso folder to your Dropbox, and then point the old location to the new synced folder. For example:

Usually, on Windows the espanso folder is located in:

C:\Users\Freddy\AppData\Roaming\espanso
After stopping espanso, you can take that folder and move it to your dropbox folder, for example:

C:\Users\Freddy\Dropbox\espanso
At this point, you want to link that new location to the old one, and this can be done with various commands depending on the OS. In particular:

Windows
Open the Command Prompt and type the following command, making sure the paths are correct

mklink /J "C:\Users\Freddy\AppData\Roaming\espanso" "C:\Users\Freddy\Dropbox\espanso"
details - https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/mklink


macOS and Linux
Open the terminal and type:

ln -s /home/alan/code/espanso_snippets/ /home/alan/.config/espanso

ln -s "/Users/user/Dropbox/espanso" "/Users/user/Library/Preferences/espanso"
If you want to sync packages as well, you have to do another step, but I'll keep it for the official documentation.

espanso start
