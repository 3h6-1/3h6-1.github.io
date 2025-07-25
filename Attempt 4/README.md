# WebKit-Bug-256172
Safari 1day RCE Exploit, might be patched in iOS 16.5.1/macOS 13.4.1</br>
Confirmed exploit works on macOS 13.3.1, iOS 15.8.2.

## Description
Currently only works on iOS 15.4.1 (iPhone 6s) due to hardcoded offsets.
- Implemented addrof/fakeobj, r/w primitive
- Execute stage1.bin by calling jitWriteSeparateHeaps since could't have RWX permissions

## Credit
- [ENKI WhiteHat](https://medium.com/@enki-techblog/ios-16-5-1-safari-rce-analysis-cve-2023-37450-89bb8583bebc) for original PoC with detail writeup
- [saelo](https://github.com/saelo/jscpwn)'s jscpwn module
- [ret2](https://github.com/ret2/Pwn2Own-2021-Safari/tree/main/eop) for building stage1.bin shellcode 
- [JakeBlair420](https://github.com/JakeBlair420/totally-not-spyware) Arbitrary call technique (up-to 4 arguments) and Mach-O parser

## Disclaimer
This repository is intended solely for educational purposes and should not be used for any malicious activities.</br>
There's no way responsible for me to any misuse of this PoC.