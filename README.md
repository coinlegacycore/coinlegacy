# Coinlegacy


# Compile on Linux Ubuntu 16
## 1. Install dependencies

run an update
`sudo apt-get update`

get all dependencies
`sudo apt-get install -y build-essential python-dev gcc g++ git cmake librocksdb-dev libboost-all-dev`

## 2. Clone the source

`git clone https://github.com/coinlegacycore/coinlegacy.git coinlegacy`

## 3. CHMOD

navigate to:
cd coinlegacy/external/rocksdb/build_tools

execute the following commands:
`chmod +x build_detect_platform`

`chmod +x version.sh`

## 4. Build executables

Back to main repo folder

cd

cd coinlegacy

prepare the build
`mkdir build && cd build`

`cmake ..`

Export flags
`export CXXFLAGS="-std=gnu++11"`

Make/Build

make
or 
make -j4

Your executables will be located in build/src folder.

# Compile on Linux Ubuntu 14

## 1. Install dependencies

run an update
`sudo apt-get update`

get all dependencies
`sudo apt-get install -y build-essential python-dev git cmake libboost1.55-all-dev libgflags-dev libsnappy-dev zlib1g-dev libbz2-dev libgflags-dev libgflags2 gcc-4.8 g++-4.8`

## 2. Install RocksDB database

`git clone https://github.com/facebook/rocksdb.git`

cd rocksdb

`make all`

## 3. Clone the source

cd

`git clone https://github.com/coinlegacycore/coinlegacy.git coinlegacy`

## 4. CHMOD

navigate to:
cd coinlegacy/external/rocksdb/build_tools

execute the following commands:
`chmod +x build_detect_platform`

`chmod +x version.sh`

## 5. Build executables

Back to main repo folder

cd

cd coinlegacy

prepare the build
`mkdir build && cd build`

`cmake ..`

Export flags
`export CXXFLAGS="-std=gnu++11"`

Make/Build
`make`

# Compile on Windows

## 1. Environment

Visual Studio 2017 Community Edition with desktop development with C++ and the VC++ v140 toolchain features selected
Boost 1.59.0, with the installer for MSVC 14

## 2. Build

From the start menu, open 'x64 Native Tools Command Prompt for vs2017'
cd <coinlegacy_directory>

mkdir build

cd build

Set the PATH for Cmake:
set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%

Run Cmake:
`cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=C:/local/boost_1_59_0`

Build:
MSBuild Coinlegacy.sln /p:Configuration=Release /m

Your binaries will be located in ..\build\src\Release folder.

# Credits
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Developers
