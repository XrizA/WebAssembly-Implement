WebAssembly
Emscripten

Emscripten:Emscripten is a toolchain for compiling to asm.js and WebAssembly, built using LLVM, that lets you run C and C++ on the web at near-native speed without plugins.
 Install Emscripten
  git clone https://github.com/emscripten-core/emsdk.git
  cd emsdk
  ./emsdk install latest
  ./emsdk activate latest
  source ./emsdk_env.sh
 Install Binaryen
  cd emsdk
  ./emsdk install binaryen-master-64bit
  ./emsdk activate binaryen-master-64bit

Compile the entire OpenCV library to WebAssembly
 requirement:Emscripten, WSL(Windows SubSystem for Linux)+Ubutus+VSCODE Install Extends(Remote-WSL)
 git clone https://github.com/opencv/opencv.git
  Build opencv.js
 cd opencv
 python ./platforms/js/build_js.py build_wasm --build_wasm --emscripten_dir /home/xriza/emsdk/upstream/emscripten
 Terimal ↓
 ====
 ==== Build finished
 ====
 OpenCV.js location /home/xriza/emsdk/opencv/build_wasm/bin/opencv.js

Compile the Dlib library to WebAssembly
 git clone https://github.com/davisking/dlib.git
 cd dlib
 mkdir build
 cd build
 cmake ..
 cmake --build . --config Release
 make install
 ldconfig
 cd ..