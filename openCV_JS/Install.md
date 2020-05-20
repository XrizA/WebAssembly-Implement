WebAssembly
Emscripten

Compile the entire OpenCV library to WebAssembly
 requirement:Emscripten, WSL(Windows SubSystem for Linux)+Ubutus+VSCODE Install Extends(Remote-WSL)
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
  Install OpenCV
   git clone https://github.com/opencv/opencv.git
  Build opencv.js
   cd opencv
   python ./platforms/js/build_js.py build_wasm --build_wasm --emscripten_dir /home/xriza/emsdk/upstream/emscripten
   ====
   ==== Build finished
   ====
   OpenCV.js location /home/xriza/emsdk/opencv/build_wasm/bin/opencv.js