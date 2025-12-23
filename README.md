# PeppyMeter Templates

Community collection of meter skins and spectrum visualizations for [PeppyMeter Screensaver](https://github.com/foonerd/peppy_screensaver).

## Repository Structure

```
template_peppy/           - VU meters only
templates_peppy_spectrum/ - VU meters with spectrum overlay
templates_spectrum/       - Spectrum analyzers only

Each category contains:
  [width]/
    [height]/
      [template-name]/
        meters.txt (or spectrum.txt)
        *.png, *.jpg
        preview.jpg
        README.md
```

## Folder Hierarchy

Templates organized by width, then height:

| Width | Heights | Resolutions |
|-------|---------|-------------|
| 0640 | - | 640x480 and variants |
| 0800 | 480, 600 | 800x480, 800x600 |
| 1024 | 600, 768 | 1024x600, 1024x768 |
| 1280 | 720, 800 | 1280x720, 1280x800 |
| 1366 | 768 | 1366x768 |
| 1480 | 320 | 1480x320 (wide displays) |
| 1920 | 1080 | 1920x1080 |

## Categories

### template_peppy
VU meter skins without spectrum analyzer. Circular (needle) or linear (bar) meters with optional metadata overlay.

### templates_peppy_spectrum
Combined VU meter and spectrum analyzer. Both visualizations displayed simultaneously.

### templates_spectrum
Spectrum analyzer only. Bar graphs, pipes, with optional reflections.

## Installation

### Single Template

1. Navigate to desired template
2. Download the template folder
3. Copy to Volumio:

```bash
scp -r template-folder volumio@volumio.local:/data/INTERNAL/peppy_screensaver/templates/
```

4. Select in plugin settings

### Sparse Checkout (Specific Resolution)

```bash
git clone --depth=1 --filter=blob:none --sparse https://github.com/foonerd/peppy_templates.git
cd peppy_templates
git sparse-checkout set template_peppy/0800/480
```

### Full Clone

```bash
git clone --depth=1 https://github.com/foonerd/peppy_templates.git
```

## Template Locations on Volumio

```
/data/INTERNAL/peppy_screensaver/templates/
```

Copy template folders directly to this location.

## Documentation

- [VU Meter Configuration](docs/METERS.md)
- [Spectrum Configuration](docs/SPECTRUM.md)
- [Template README Template](docs/TEMPLATE_README.md)
- [Contributing Guide](CONTRIBUTING.md)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for submission guidelines.

### Quick Checklist

- [ ] Place in correct path: `[category]/[width]/[height]/[name]/`
- [ ] Include meters.txt or spectrum.txt
- [ ] Include preview.jpg
- [ ] Include README.md
- [ ] Test on hardware

## Credits

- Original PeppyMeter: [project-owner](https://github.com/project-owner)
- Original PeppySpectrum: [project-owner](https://github.com/project-owner)

## License

Individual templates may have their own licenses. See each template's README.

## Related

- [PeppyMeter Screensaver Plugin](https://github.com/foonerd/peppy_screensaver)
- [PeppyMeter Build Tools](https://github.com/foonerd/peppy_builds)
