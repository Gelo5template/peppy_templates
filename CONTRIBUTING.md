# Contributing Templates

Thank you for contributing to the PeppyMeter template collection.

## Template Location

Place your template in the correct path:

```
[category]/[width]/[height]/[template-name]/
```

**Categories:**
- `template_peppy` - VU meters only
- `templates_peppy_spectrum` - VU meters with spectrum
- `templates_spectrum` - Spectrum only

**Example:**
```
template_peppy/0800/480/retro-wood/
  meters.txt
  preview.jpg
  README.md
  retro-wood-bgr.png
  retro-wood-fgr.png
  retro-wood-needle.png
```

## Required Files

| File | Required | Description |
|------|----------|-------------|
| meters.txt / spectrum.txt | Yes | Configuration |
| preview.jpg | Yes | Screenshot |
| README.md | Yes | Description and credits |
| Graphics files | Yes | PNG/JPG assets |

## Naming Convention

Template folder names:
- Lowercase
- Hyphens for spaces
- No version numbers
- Descriptive but concise

Good: `mcintosh-mc275`, `neon-blue`, `retro-vfd`
Bad: `My Template v2`, `FINAL_template`

## Preview Image

- Filename: `preview.jpg`
- Size: Proportional to resolution (~400px wide)
- Show template with sample metadata
- Under 100KB

## Submission Process

1. Fork repository
2. Create branch: `git checkout -b add-template-name`
3. Add template to correct path
4. Test on hardware
5. Commit: `git commit -m "Add template-name for WIDTHxHEIGHT"`
6. Push and create Pull Request

## Pull Request Description

Include:
- Template name and resolution
- Category (peppy/peppy_spectrum/spectrum)
- Hardware tested on
- Credits for external assets

## Quality Checklist

- [ ] Works at target resolution
- [ ] No visual glitches
- [ ] Reasonable CPU usage
- [ ] All text readable
- [ ] Tested on actual hardware

## Asset Guidelines

| Type | Format | Notes |
|------|--------|-------|
| Background | PNG/JPG | Match resolution |
| Foreground | PNG | Requires transparency |
| Needle/Bar | PNG | Requires transparency |
| Preview | JPG | Compressed |

## Questions

Open an issue with `question` label.
