Maybe oh my zsh work slowly in your computer and you don't like your prompt. try this. It's useful for me 😁.

![Screenshot 2022-02-02 at 17 36 14](https://user-images.githubusercontent.com/38573357/152196730-93a67eda-0e49-4cf9-b985-e7930d7dce2a.png)

# How to use

## Download the Repo

Move file `.bash_prompt` in the same route of you `.bashrc` or `.zshrc`

## Or  Create file `.bash_prompt`.

write in the file `.bash_prompt`:

```
PROMPT="🤘 %F{cyan}%c%f %F{green}$%f "

autoload -Uz vcs_info
precmd_vcs_info() { vcs_info }
precmd_functions+=( precmd_vcs_info )
setopt prompt_subst
RPROMPT='${vcs_info_msg_0_}'

zstyle ':vcs_info:git:*' formats '📍 %F{red}%b%f'
```

## Add in your `.bashrc` or `.zshrc`

```
if [ -f ~/.bash_prompt ]; then . ~/.bash_prompt; fi
```

## At last

```
source .bashrc
# or
source .zshrc
```

🥳
