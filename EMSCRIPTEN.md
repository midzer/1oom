# Emscripten

## Build

```
autoreconf -fi
mkdir build-native
cd build-native
emconfigure ../configure
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions ui/classic/*.o hw/sdl/2/*.o os/unix/*.o */*.o *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["mid"]' -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@../../funcs.txt -sENVIRONMENT=web --preload-file backgrnd.lbx --preload-file colonies.lbx --preload-file council.lbx --preload-file design.lbx --preload-file diplomat.lbx --preload-file embassy.lbx --preload-file eventmsg.lbx --preload-file firing.lbx --preload-file fonts.lbx --preload-file help.lbx --preload-file intro.lbx --preload-file intro2.lbx --preload-file introsnd.lbx --preload-file landing.lbx --preload-file missile.lbx --preload-file music.lbx --preload-file names.lbx --preload-file nebula.lbx --preload-file newscast.lbx --preload-file planets.lbx --preload-file reqd.lbx --preload-file research.lbx --preload-file screens.lbx --preload-file ships.lbx --preload-file ships2.lbx --preload-file snddrv.lbx --preload-file soundfx.lbx --preload-file space.lbx --preload-file spies.lbx --preload-file starmap.lbx --preload-file starview.lbx --preload-file techno.lbx --preload-file v11.lbx --preload-file vortex.lbx --preload-file winlose.lbx --preload-file dgguspat/ --preload-file timidity.cfg --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
