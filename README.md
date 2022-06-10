# Compile Crypto++ Library
Open Crypto++ Solution and Compile cryptlib project to generate static library file with Debug  or Releasewith Win32 settings
../cryptopp850/cryptest.sln


Your output will be located at

..\cryptopp850\Win32\Output\Debug\cryptlib.lib


# Compile and Run Sample Application

Open crypto test application

../CryptoppTestApplication/CryptoppTestApplication.sln


All static library path configurations are placed in CryptoppStaticLibraryUsageSample.cpp file as follow, check static library path is correct for your solution. Path is relative. 

#ifdef _DEBUG
#pragma comment(lib, "../../cryptopp850/Win32/Output/Debug/cryptlib.lib")
#else
#pragma comment(lib, "../../cryptopp850/Win32/Output/Release/cryptlib.lib") 
#endif
#define CRYPTOPP_ENABLE_NAMESPACE_WEAK 1
#include "../../cryptopp850/cryptlib.h"
#include "../../cryptopp850/sha.h"
#include "../../cryptopp850/hex.h"
#include "../../cryptopp850/files.h"
#include "../../cryptopp850/rijndael.h"
#include "../../cryptopp850/modes.h"
#include "../../cryptopp850/osrng.h"
#include "../../cryptopp850/md5.h"
#include "../../cryptopp850/crc.h"
#include "../../cryptopp850/des.h"
#include <iostream>
#include <string>
using namespace std;
using namespace CryptoPP;
  
