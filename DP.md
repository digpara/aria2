## pre dep
xcode-select --install 
brew install autoconf automake
autoreconf -i # if no configure

## build
./configure ARIA2_STATIC=yes
make -j8
make install
