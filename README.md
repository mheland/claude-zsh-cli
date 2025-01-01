# CLI interface for Claude with Z Shell
Claude AI with ZSH, call using `@ai Hello Claude!`

- Uses Claude Haiku for fast response.
- Python3 for parsing JSON respons, grep fallback
- `--debug` to see raw response

## Install jq for JSON parsing
`sudo apt-get install jq`

## Add to path
Save script in `~/bin` and add to $PATH if not already there, or symlink 

`sudo ln -s /path/to/claude-cli /usr/local/bin/@ai`

First run will ask for your Claude API key and store in `$HOME/.config/claude-cli/config`

## AI CLI alias and completion in .zshrc
```
  alias @ai="noglob claude-cli"  
  compdef _gnu_generic @ai
```

`noglob` so you can add a questionmark at the end

## Ain't workin?
Run with --debug ex 

`@ai --debug "Hello Claude!"`
