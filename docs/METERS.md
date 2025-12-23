# VU Meter Configuration Reference

Complete reference for meters.txt configuration.

## File Structure

```ini
[meter-name]
meter.type = circular
channels = 2
ui.refresh.period = 0.033
bgr.filename = meter-bgr.png
fgr.filename = meter-fgr.png
indicator.filename = meter-needle.png
screen.bgr = meter-ext.jpg
meter.x = 0
meter.y = 100

# --- volumio optional entries -------
config.extend = True
```

## Meter Types

### Circular (Needle)

```ini
[example-circular]
meter.type = circular
channels = 2
ui.refresh.period = 0.033
bgr.filename = meter-bgr.png
fgr.filename = meter-fgr.png
indicator.filename = meter-needle.png
start.angle = 45
stop.angle = -45
steps.per.degree = 4
distance = 100
left.origin.x = 200
left.origin.y = 200
right.origin.x = 600
right.origin.y = 200
meter.x = 0
meter.y = 100
screen.bgr = meter-ext.jpg
```

### Linear (Bar)

```ini
[example-linear]
meter.type = linear
channels = 2
ui.refresh.period = 0.033
bgr.filename = meter-bgr.png
fgr.filename = meter-fgr.png
indicator.filename = meter-indicator.png
left.x = 20
left.y = 50
right.x = 20
right.y = 150
position.regular = 10
position.overload = 2
step.width.regular = 8
step.width.overload = 8
direction = left-right
meter.x = 0
meter.y = 0
screen.bgr = meter-ext.jpg
```

## Core Settings

| Key | Type | Description |
|-----|------|-------------|
| meter.type | string | circular or linear |
| channels | int | 1 or 2 |
| ui.refresh.period | float | Frame time (0.033 = 30fps) |

## Volumio Extended Configuration

Enable with `config.extend = True`

### Album Art

```ini
albumart.pos = 20,20
albumart.dimension = 200,200
albumart.border = 1
albumart.mask = mask.jpg
albumart.rotation = True
albumart.rotation.speed = 6
```

### Track Information

```ini
playinfo.title.pos = 250,30,bold
playinfo.title.color = 255,255,255
playinfo.title.maxwidth = 400

playinfo.artist.pos = 250,60,regular
playinfo.artist.color = 200,200,200
playinfo.artist.maxwidth = 400

playinfo.album.pos = 250,90,light
playinfo.album.color = 180,180,180
playinfo.album.maxwidth = 400

playinfo.center = False
```

Position format: X,Y,style (bold/regular/light)

### Fonts

```ini
font.size.digi = 28
font.size.light = 14
font.size.regular = 16
font.size.bold = 18
font.color = 255,255,255
```

### Time and Format

```ini
time.remaining.pos = 700,120
time.remaining.color = 255,255,255

playinfo.type.pos = 700,30
playinfo.type.color = 255,255,255
playinfo.type.dimension = 32,32

playinfo.samplerate.pos = 700,70,regular
playinfo.samplerate.maxwidth = 130
```

### Spectrum Overlay

```ini
spectrum.visible = True
spectrum.name = s.1
spectrum.size = 800,150
```

## Deprecated Settings

| Setting | Replacement |
|---------|-------------|
| playinfo.maxwidth | Use playinfo.title.maxwidth, etc. |
