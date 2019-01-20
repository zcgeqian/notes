## Git notes

- start new session

`screen -S sessionname`

- detach and kill session:

`$ screen -X -S [session # you want to kill] quit`

- detach current session

`$ screen -d [session id]`

- switch to other session

`$ screen -r session id`

- show sessions

`$ screen -r`

`screen -list`

## GCC降级
`sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 100`

```

```