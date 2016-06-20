
Mojocoin is a PoS-based cryptocurrency.

Mojocoin uses libsecp256k1,
			  libgmp,
			  Boost1.55,
			  OR Boost1.57,  
			  Openssl1.01p,
			  Berkeley DB 4.8,
			  libevent,
			  QT5 to compile


Block Spacing: 60 Seconds
Stake Minimum Age: 24 Hours

Port: 22255
RPC Port: 22254


BUILD LINUX
-----------
1) git clone https://github.com/stormbitz/Mojocoin.git mojocoin

2) cd mojocoin/src

3) sudo make -f makefile.unix            # Headless mojocoin

(optional)

4) strip mojocoind

5) sudo cp mojocoind /usr/local/bin




BUILD WINDOWS
-------------

1) Download Windows Build Environment.rar from https://github.com/Infernoman/Transfercoin/releases/tag/WBE and unpack to C:/

2) Download Mojocoin source https://github.com/stormbitz/Mojocoin/archive/master.zip 

2.1) Unpack to C:/Mojocoin

3) Install Perl for windows from the homepage http://www.activestate.com/activeperl/downloads

4) Download Python 2.7 https://www.python.org/downloads/windows/

4.1) While installing python make sure to add python.exe to the path.

5) Run msys.bat located in C:\MinGW49-32\msys\1.0

6) cd /C/Mojocoin/src/leveldb

7) Type "TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a" and hit enter to build leveldb

8) Exit msys shell

9) Open windows command prompt

10) cd C:/dev

11) Type "49-32-qt5.bat" and hit enter to run

12) cd ../Mojocoin

13) Type "qmake USE_UPNP=-" and hit enter to run

14) Type "mingw32-make" and hit enter to start building. When it's finished you can find your .exe in the release folder.