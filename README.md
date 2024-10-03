# dot_files

This project is used for storing .config files.

## Getting Started
1. Add the following to your ~/.bashrc (bash configuration file)

``` 
#alias
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

# functions
if [ -f ~/.bash_funcions ]; then 
    . ~/.bash_functions
fi 

#env vars
export $(grep -v '^#' ~/.env | xargs)
```

2. Softlink the files to `~/`:
    1. .bash_aliases
    2. .bash_functions

    Make `.env` to store env vars:
    ```
    touch ~/.env
    ```

3. Source ~/.bashrc