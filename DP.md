## pre dep
xcode-select --install 
autoreconf -i # if no configure

## build
./configure ARIA2_STATIC=yes
make -j8
make install
