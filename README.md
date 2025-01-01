# claude-zsh-cli
Claude AI with ZSH, call using `@ai Hello Claude!`

## Install jq for JSON parsing
`sudo apt-get install jq`

## Add to path
Save script in `~/bin` and add to $PATH if not already there, or symlink 

`sudo ln -s /path/to/claude-cli /usr/local/bin/@ai`

First run will ask for your Claude API key and store in `$HOME/.config/claude-cli/config`

## AI CLI alias and completion in .zshrc
`alias @ai="claude-cli"`

`compdef _gnu_generic @ai`

## Ain't workin?
Run with --debug ex 

`@ai --debug "Hello Claude!"`
