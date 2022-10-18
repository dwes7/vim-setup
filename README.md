### Install Vundle

```
mkdir ~/.vim/bundle
cd ~/.vim/bundle
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
mkdir vimrc_repo
cd vimrc_repo
git clone git@github.com:dwes7/.vimrc.git
cp .vimrc/.vimrc ~/.vimrc
```

Open vim and run:
```
:PlugInstall
```

Boom you got your default vim environment.


### Clone and Build CCLS from source
Link to clone and build instructions for CCLS
[here|https://github.com/MaskRay/ccls/wiki/Build]
```
git clone --depth=1 --recursive https://github.com/MaskRay/ccls
cd ccls
# Download "Pre-Built Binaries" from https://releases.llvm.org/download.html
# and unpack to /path/to/clang+llvm-xxx.
# Do not unpack to a temporary directory, as the clang resource directory is hard-coded
# into ccls at compile time!
# See https://github.com/MaskRay/ccls/wiki/FAQ#verify-the-clang-resource-directory-is-correct
cmake -H. -BRelease -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=/path/to/clang+llvm-xxx
cmake --build Release
```





