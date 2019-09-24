## pre dep
xcode-select --install 
brew install autoconf automake gettext libtool docutils 

ln -s /usr/local/bin/rst2html.py /usr/local/bin/rst2html

export PATH=${PATH}:/usr/local/opt/gettext/bin
autoreconf -i # if no configure

## build
./configure --prefix=/usr/local --without-libxml2 --enable-static --disable-shared ARIA2_STATIC=yes
make -j8
make install
