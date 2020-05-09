# SDL_ttf for PSP

Requirements:

 - freetype
 - SDL

Build procedure:

```shell
./autogen.sh
LDFLAGS="-L$(psp-config --pspsdk-path)/lib" LIBS="-lc -lpspuser" \
  ./configure --host psp --with-sdl-prefix=$(psp-config --psp-prefix) \
  --with-freetype-prefix=$(psp-config --psp-prefix) \
  --without-x --prefix=$(psp-config --psp-prefix)
make
make install
```
