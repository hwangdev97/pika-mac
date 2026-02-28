# pika-mac

Slap your MacBook, Pikachu responds!

<video src="demo.mp4" controls width="300"></video>

Detects physical impacts on Apple Silicon MacBooks via the built-in accelerometer (Bosch BMI286 IMU) and plays Pikachu sound effects. Requires `sudo`.

> Inspired by [taigrr/spank](https://github.com/taigrr/spank). The accelerometer access and vibration detection algorithms come from that project. pika-mac replaces the audio with Pikachu-themed sounds and adds battle / happy modes.

## Usage

```bash
# Default mode — random Pikachu cries
sudo pika-mac

# Battle mode — Thunderbolt!
sudo pika-mac --battle

# Happy mode — the more you slap, the happier Pikachu gets (escalates over a 5-min window)
sudo pika-mac --happy
```

## Build

```bash
go build -o pika-mac .
```

## Credits

- [taigrr/spank](https://github.com/taigrr/spank) — the original project that provides accelerometer access and vibration detection
- [taigrr/apple-silicon-accelerometer](https://github.com/taigrr/apple-silicon-accelerometer) — Apple Silicon accelerometer library

---

[中文说明](README_CN.md)
