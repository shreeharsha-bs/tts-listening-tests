# TTS Subjective Listening Tests Demo

Interactive web demo of 6 common subjective evaluation methods for Text-to-Speech (TTS) systems. Designed for educational use in speech technology courses.

## 🎧 Live Demo

Visit: **[Your GitHub Pages URL]**

## Test Types

| Test | Description | Output |
|------|-------------|--------|
| **MOS** | Mean Opinion Score — absolute rating (1–5) | Single naturalness score |
| **CMOS** | Comparative MOS — relative rating (−3 to +3) | Preference strength between A and B |
| **AB** | Forced choice preference test | Binary choice |
| **ABX** | Identification test — is X same as A or B? | Correct/incorrect identification |
| **MUSHRA** | Multi-stimulus with hidden reference and anchor (0–100) | Multiple system ratings |
| **Best-Worst** | Select best and worst from a block of 4 | Implicit pairwise preferences |

## Audio File Structure

Audio files follow this naming convention:

```
{theme}_{register}_{style}_{voice}_{resonance}.wav
```

Where:
- **theme**: `sent01` (sun), `sent02` (chess), `sent03` (winter)
- **register**: `formal`, `informal`
- **style**: `clear`, `spont` (spontaneous)
- **voice**: `male`, `female`, `amb` (ambiguous)
- **resonance**: `res` (resonant), `nonres` (non-resonant)

Example: `sent01_formal_clear_female_res.wav`

## Usage

1. Open `index.html` in a browser (or visit the GitHub Pages URL)
2. Click "Select Audio Folder" and choose the `timeless_test` folder
3. Select a theme from the dropdown
4. Navigate through the tabs to try each test type
5. Download your results as JSON when finished

## Local Development

Simply serve the files with any static server:

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve
```

Then open `http://localhost:8000`

## File Structure

```
├── index.html          # Main demo page
├── README.md           # This file
└── timeless_test/      # Audio samples (72 WAV files)
    ├── sent01_*.wav    # Theme 1 (Sun)
    ├── sent02_*.wav    # Theme 2 (Chess)
    └── sent03_*.wav    # Theme 3 (Winter)
```

## References

- ITU-T P.800 (MOS)
- ITU-R BS.1534 (MUSHRA)
- Loizou, P. C. (2011). Speech Quality Assessment
- Tånnander et al. (2025). Best-Worst Scaling for TTS Evaluation

## License

Educational use only. Audio samples are synthetic speech demonstrations.
