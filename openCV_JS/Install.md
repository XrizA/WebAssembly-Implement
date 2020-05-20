Emscripten
=
Install Emscripten
-
  >git clone https://github.com/emscripten-core/emsdk.git <br />
  cd emsdk <br />
  ./emsdk install latest <br />
  ./emsdk activate latest <br />
  >source ./emsdk_env.sh <br />

Install Binaryen <br />
-
  >cd emsdk <br />
  ./emsdk install binaryen-master-64bit <br />
  ./emsdk activate binaryen-master-64bit

Compile the entire OpenCV library to WebAssembly
=
 **requirement:Emscripten, WSL(Windows SubSystem for Linux)+Ubutus+VSCODE Install Extends(Remote-WSL)** <br />
 
 git clone https://github.com/opencv/opencv.git <br />

Build opencv.js
-
 >cd opencv <br />
 python ./platforms/js/build_js.py build_wasm --build_wasm --emscripten_dir /home/xriza/emsdk/ >upstream/emscripten <br />

Console ↓
-
 >Build finished <br />
 OpenCV.js location /home/xriza/emsdk/opencv/build_wasm/bin/opencv.js
 

Compile the Dlib library to WebAssembly
=
 >git clone https://github.com/davisking/dlib.git <br />
 cd dlib <br />
 mkdir build <br />
 cd build <br />
 cmake .. <br />
 cmake --build . --config Release <br />
 make install <br />
 ldconfig <br />
 cd .. <br />