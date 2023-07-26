# RTMP-Live-Stream-Server

RTMP live stream server

# How To Use

<b>Local</b> <br />

1.  Run project:

- Clone or download repo and unzip
- Install packages

```
npm install
```

- Start

```
npm run start
```

3. RTMP Stream:

- Start the rtmp server to allow subscribers watch streams
- <a href="https://github.com/ConfidenceDev/RTMP-Live-Stream-Server">https://github.com/ConfidenceDev/RTMP-Live-Stream-Server</a>
- Update <b>rtmpUrl</b> in <b>app.js</b> code if RTMP server is not running on localhost (Eg: If running rtmp server in a container, change rtmp url with conatiner IP Address and port or setup a docker network)

4. Watch Stream:

- Use any client that can play rtmp stream and pass the url:
  <b>rtmp://localhost/live/stream</b>
- Use VLC: Open VLC -> Select Media -> Select Open Network Stream and paste stream url.

<br />

<b>Docker</b>

1. build docker image

```
docker build -t <image-name> .
```

2. Start container:

```
docker run -d -p 1935:1935 -p 8000:8000 --name <container-name> <image-name>:latest
```
