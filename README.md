## A Simple Browser Audio/Video Chat Using Peer.js

The page index.html contains javascript code to access the WebRTC technology of modern browsers. WebRTC enables encrypted peer-to-peer audio/video/data connections with the support of special servers to penetrate routers and firewalls. This implementation uses the portable Peer.js wrapper from http://peerjs.com and the free peer server provided by them.

For security reasons, the page index.html must be served to your browser from your local system.

### Installation and Operation

1. Download `index.html`
1. Get a free API key from http://peerjs.com/peerserver
1. Replace MY_KEY in `index.html` with your key
1. Open a terminal console and `cd` to the directory where `index.html` resides
1. Start a basic server. Two possible variations:
  * `$ ncat -lk -p 8000 --sh-exec "echo -e 'HTTP/1.1 200 OK\r\n'; cat index.html"`
  * `$ python -m http.server 8000`
1. In a browser that supports WebRTC, enter the URL [http://localhost:8000](http://localhost:8000)
  * Use the URL [http://localhost:8000?novid](http://localhost:8000?novid) for an audio-only chat
1. When prompted for your ID, enter an identifying string with no spaces
1. When prompted for the ID of your chat partner:
  * Enter his/her ID to initiate an outgoing call to him/her (if already online)
  * Enter a blank to wait for an incoming call
1. Upon an incoming call, an alert will give the caller ID and await your permission to chat
