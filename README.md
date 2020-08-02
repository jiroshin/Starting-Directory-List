# Starting Directory List
command `sdl` returns a list of directories under the environment variable `$SDL_ROOT`.  

For example, if you have the following directory structure:
```
sdl-root
├── category1
│   ├── child-category1-1
│   │   ├── child-category-1-1-1
│   │   │   └── avocado.text
│   │   ├── mango.text
│   │   └── melon.text
│   ├── child-category1-2
│   │   └── cherry.text
│   └── orange.text
└── category2
    ├── apple.text
    └── child-category2-1
        └── peach.text
```

`sdl` command execution result is as follows, when `export SDL_ROOT=$HOME/sdl-root`.
```
$ sdl
~/sdl-root/category1/
~/sdl-root/category2/
~/sdl-root/category1/child-category1-1/
~/sdl-root/category1/child-category1-2/
~/sdl-root/category2/child-category2-1/
```
`sdl` command returns a list of directories under `$SDL_ROOT` and one directory below it.  
It is a good idea to use the directory one level below as a namespace.

## How to use
1. git clone and pass the path to sdl.
```
$ git clone https://github.com/jiroshin/Starting-Directory-List.git
$ echo export PATH='{{PATH-WHERE-YOU-CLONED}}/:$PATH' >> ~/.bash_profile
```

2. Give the command execute permission.
```
$ chmod 777 {{PATH-WHERE-YOU-CLONED}}/sdl
```

3. Set the directory you want to handle with an environment variable.
```
$ echo export SDL_ROOT='$HOME/dev' >> ~/.bash_profile
```
