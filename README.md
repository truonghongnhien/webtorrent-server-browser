# webtorrent-server-browser
test `torrent.createServer()` using service worker

demo: https://tr.github.io/webtorrent-server-browser/

# Motivation
Using html video MSE to decode/encode a video in order to support streaming/seaking with javascript is a bit slower.
Using MSE means we have to support more containers manually like mp4 or webm for example. 

Serving a file directly to a video element as if where a regular url will let the browser handle seeking, making range request, and encode it much faster. that probably also means more support for other media containers

Doing this makes you wonder if you even need this packages at all:

- mp4-box-encoding
- mp4-stream
- mediasource
- render-media
- videostream
- range-slice-stream
- stream-to-blob-url
