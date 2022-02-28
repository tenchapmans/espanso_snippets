# **espanso_snippets**

place to store the espanso yml files I use.

Some pulled from other git repos:

https://github.com/Lissy93/espanso-config

https://github.com/ekiel/espanso/blob/master/default.yml

Notes
The key is to use symbolic links, which are available in all operating systems. The idea is to move your espanso folder to your Dropbox, and then point the old location to the new synced folder. For example:

Usually, on Windows the espanso folder is located in:

C:\Users\Freddy\AppData\Roaming\espanso
After stopping espanso, you can take that folder and move it to your dropbox folder, for example:

C:\Users\Freddy\Dropbox\espanso
At this point, you want to link that new location to the old one, and this can be done with various commands depending on the OS. In particular:

## **Linux**

Open the terminal and type:

`espanso stop`

`git clone https://github.com/tenchapmans/espanso_snippets.git ~/git/espanso`

`ln -s ~/git/espanso/ ~/.config/espanso`

`espanso start`

## **Windows**

Open the Command Prompt and type the following command, making sure the paths are correct

```
`espanso stop`
mklink /J "C:\Users\acchapm1\AppData\Roaming\espanso" "D:\git\espanso"
`espanso start`
```

**Example:**
`mklink /J C:\LinkToFolder C:\Users\Name\OriginalFolder`
`mklink /J  [link] [source]`  (put in quotes " " if there are spaces)




