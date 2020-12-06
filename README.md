# Roku-Fiddler-Example
Step by step on how to configure Fiddler and a development Roku to examine Roku network traffic

As the developer for the lastest [SomaFM](https://channelstore.roku.com/details/35082ffbffa265fefd5c7a8e2c84f875/somafm) app on the Roku platform I had the need to examine and control the network traffic to and from the Roku I was using for development. 

To do this I needed to stand up a network proxy and direct the Roku network traffic to it. My choice of proxy was [Fiddler](https://www.telerik.com/download/fiddler) from Telerik. Telerik provides two varieties of Fiddler, Fiddler Everywhere, which runs on Windows, Mac and Linux, and Fiddler Classic, which is Windows only. I chose to use Fiddler Classic, since I was familiar with it and I was going to use a Windows to host the proxy. In my case I installed Fiddler on a VM on my network but you can install it locally if needed. I chose a separate system in order to better isolate network activity and configuration.

<h3>Download and install Fiddler</h3> This is straightforward, just run the FiddlerSetup.exe installer. 

<h3>Configure Fiddler</h3>
Open Fiddler and go to Tools -> Options and selected the Connections tab. Check **Allow remote computers to connect**. This enable Fiddler to accept connections from the Roku.
