# PoGoMITM [![Build status](https://ci.appveyor.com/api/projects/status/iipbt2ftxv7w49dh/branch/master?svg=true)](https://ci.appveyor.com/project/TBulbaDB/pogomitm/branch/master)

This project is a .net MITM proxy designed to read all the API messages sent between the Pokemon Go device and the Pokemon Go servers. 

![PoGoMITM WebUI Screenshot](https://raw.githubusercontent.com/TBulbaDB/PoGoMITM/master/PoGoMITM-WebUI.png)

# Support

Use the [Issues](https://github.com/TBulbaDB/PoGoMITM/issues) or catch me on [Discord](https://discord.gg/3UtF8W6)

# Usage

## Running for the first time

It's important that you run it as Administrator. 

If you are using the precompiled release package, just run PoGoMITM.exe. If you are using the source, you should already know what to do. :)

It will create a root certificate and ask you if you want to install it. Click to Yes. After that, goto http://localhost:61222 and you should see the Web UI.

## Setting up your Android Phone to use the proxy

After making sure that the Proxy and Web UI running (see the console output for detailed info), go to your Phone Settings / WiFi, find your WiFi connection. Tap on it and wait a bit till you see the menu with Modify Network option. In Modify Network, you should see Advanced options, and a Proxy option under it. Select Manual as Proxy, then enter the ip address of your Proxy Server (the local ip of the computer you are running the Proxy server) and 61221 as port. *It's important that you add storage.google.com to Proxy Bypass List on your WIFI connection's settings.*

Then open a web browser on your phone and enter http://proxyip:61222. You should see the Web UI. There click to Download Root Certificate link at the top right corner and follow the instructions to install the certificate.

You also need the PoGo APK with Certificate Pinning disabled in order to run PoGo through the proxy. You can download it here: https://github.com/rastapasta/pokemon-go-mitm/issues/69#issuecomment-238457389

See https://github.com/rastapasta/pokemon-go-mitm#setting-up-your-device for more detailed info on setting up your phone.

## Settings

All the settings are located in PoGoMITM.exe.config file (App.Config if you are using the source code)



