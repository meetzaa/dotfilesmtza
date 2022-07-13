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
  2 "languageserver": {
  3     "ccls": {
  4       "command": "ccls",
  5       "args": ["--log-file=/tmp/ccls.log", "-v=1"],
  6       "filetypes": ["c", "cc", "cpp", "c++", "objc", "objcpp"],
  7       "trace.server": "verbose",
  8       "rootPatterns": [".ccls", "compile_commands.json"],
  9       "initializationOptions": {
 10          "cache": {
 11            "directory": "/tmp/ccls"
 12          },
 13          "client": {
 14           "snippetSupport": true
 15          }
 16        }
 17     }
 18   },
 19   "clangd.path": "~/.config/coc/extensions/coc-clangd-data/install/14.0.3/cl
 20 }

Optional : brew install bear
