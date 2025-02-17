# Initial Settings
Create a `.env` file in the server/ folder and write the code according to the format below.

> In a single client (test environment), the ports of the assets(image, video) server must be different from those of the existing web server.

## The Required Properties

```env
POSTGRES_DB=pubicons
POSTGRES_PORT=5432
POSTGRES_USER=root
POSTGRES_PASSWORD=...

REDIS_PORT=6379
REDIS_PASSWORD=...{0}
```

## The Non-Required Properties
```env
# This property is not required.
AV1_ENCODER=libsvtav1

# This property is not required.
# Using CPU = libx265
# Radeon GPU = hevc_amf
# NVIDIA GPU = hevc_nvenc
H265_ENCODER=libx265

# This property is not required.
# Using CPU = libx264
# Radeon GPU = h264_amf
# NVIDIA GPU = h264_nvenc
H264_ENCODER=libx264

# This properties is not required.
BITRATE_P144=300000; ## 300kbps
BITRATE_P240=500000; ## 500kbps
BITRATE_P480=1500000; ## 1.5Mbps
BITRATE_P720=3000000; ## 3.0Mbps
BITRATE_P1080=6000000; ## 6.0Mbps
BITRATE_P1440=12000000; ## 12.0Mbps
BITRATE_P2160=25000000; ## 12.0Mbps
```

And then, create a `redis.conf` file in the server/ folder and write the code according to the format below.

```conf
requirepass ...{0}
```

# Download FFmpeg
Must download the external dependency `FFmpeg`. And extract the downloaded archive and place the contents in a directory (e.g., C:\Program Files\ffmpeg). And add the directory (e.g., C:\Program Files\ffmpeg) to the Path system environment variable.

> Need to verify the setup by running ffmpeg -version in the command prompt.

| Type | URL |
| ---- | ------ |
| Link 1 | https://www.ffmpeg.org |
| Link 2 | https://github.com/BtbN/FFmpeg-Builds [(Latest)](https://github.com/BtbN/FFmpeg-Builds/releases/tag/latest) |

# Get Started
Enter the following commands in turn in the terminal.

- `npm install`: installing NPM packages.
- `npm run build`: installing git submodule.
- `npm run alive`: initialing about docker compose.
- `npm run watch` or `npm run start`
