# Stereoscopic Video

HISPlayer SDK v2.11.0.1 and above support stereoscopic Side-By-Side (Left/Right) and Top/Bottom video rendering.

---

## HISPlayer_Blueprint Configuration

Inside the `HISPlayer_Blueprint`, stereoscopic behavior is controlled using the following setting:

### Stereo Format Array

The `Stereo Format` array defines the stereoscopic type for each video stream.

<p align="center">
  <img width="524" height="168" alt="image" src="https://github.com/user-attachments/assets/18aa7822-7fa1-49c2-92a5-edb5ed6a755e" />
</p>

Each element in this array corresponds directly to the same index in the `Stream URL` array.

---

## Stream Mapping

| Stream URL Index | Stereo Format Index | Description |
|------------------|---------------------|-------------|
| 0                | 0                   | First video stream |
| 1                | 1                   | Second video stream |
| ...              | ...                 | ... |

This means every video stream must have its matching stereoscopic configuration in the same array position.

---

## Supported Stereo Formats

The `Stereo Format` field supports the following values:

- **None**
  - No stereoscopic processing is applied.
  - Standard monoscopic video playback.

- **TopBottom**
  - Left and right views are stacked vertically.
  - Common format for stereoscopic video distribution.

- **SideBySide**
  - Left and right views are placed horizontally.
  - Widely used format for 3D video content.

---

## Notes

- Ensure `Stream URL` and `Stereo Format` arrays always have the same length.
- Incorrect indexing may lead to wrong rendering or broken 3D output.
- This configuration is applied per stream, not globally.
