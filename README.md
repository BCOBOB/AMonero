# A Monero – A Monero Miner for Android

This MY adaption of a Forked Proof of concept using the xmrig miner inside an Android APK.

Get the original source i forked from at github: https://github.com/DongAoMainland/MoneroMiner.git

Based on the code from https://github.com/xmrig/xmrig.  


# Usage

This will currently only work on devices with ARM64 architecture.

Install and run the app, enter your pool and wallet data, then press the start button
to start mining or stop to stop mining.
The help button will show xmrig's help output for convenience.
 
As this is considered a proof of concept, only pool address, username, threads and max cup usage can be
edited in the UI currently (there is currently no sanity check to your inputs). You can change the rest of the config in assets/config.json.
The configuration is set to low values and regular display of hashrate is set to 1m.  
  
# Notes
  
The xmrig binary is copied to the app's internal directory along with its dependent libraries.
(This is done because it can only be executed there.)
Then, the binary is started using the ProcessBuilder class, and the output is captured
into the app's scrolling pane once each secons.

Only arm64 binaries are included, and the app will refuse to work on 
other architectures like x86 or 32 bit devices. 

# License

xmrig is licensed as GPLv3, thus this derivative work also is.
You need to consider this if you plan to build a "real" Android app. You'd propably need
to make it GPLv3 also, unless you can somehow make use of the GPL clause which allows
to bundle a GPLv3 binary with another propietary licensed binary.

