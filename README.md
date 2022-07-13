# dotfilesmtza
My personal .dotfiles for MacOS

Setting up : 

1. Install iTerm2
2. Install Fish Shell 
3. Download Nerd Font (I use Hack)
4. Download all the necesary files.

Personal set up : 
1. Install XCode
2. Install DevCleaner for XCode (App Store)
3. Install VS Code
4. Install CLion

Other apps I may need : Numi, CleanMyMac X, iStat Menu, Magnet

You'll need to set up ccls and coc by yourself since git doesn't see the problem.

1. In terminal:  brew install ccls
2. In plug.vim: Plug 'neoclide/coc.nvim', {'branch': 'release'}
3. In nvim run: CocInstall coc-clangd
4. In CocConfig insert: 

{
   "languageserver": {
       "ccls": {
         "command": "ccls",
         "args": ["--log-file=/tmp/ccls.log", "-v=1"],
         "filetypes": ["c", "cc", "cpp", "c++", "objc", "objcpp"],
         "trace.server": "verbose",
         "rootPatterns": [".ccls", "compile_commands.json"],
         "initializationOptions": {
           "cache": {
             "directory": "/tmp/ccls"
           },
           "client": {
            "snippetSupport": true
           }
         }
      }
    },
    "clangd.path": "~/.config/coc/extensions/coc-clangd-data/install/14.0.3/cl
  }

Optional : brew install bear
