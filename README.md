# Digital Dream - Stable Diffusion Models

This repository hosts the CoreML Stable Diffusion models for the [Digital Dream visionOS app](https://github.com/smaerdlatigid/digital-dream-visionOS).

## Models

### Unet Model (v0.3.1)
- **File**: `Unet.mlmodelc.tar.gz`
- **Size**: 1.5 GB (compressed)
- **Usage**: CoreML Stable Diffusion Unet model for on-device image generation

## Download

Models are available as GitHub Release assets:

- [Download Unet v0.3.1](https://github.com/YOUR_USERNAME/digital-dream-models/releases/download/v0.3.1/Unet.mlmodelc.tar.gz)

## Installation (for developers)

1. Download the tarball
2. Extract: `tar -xzf Unet.mlmodelc.tar.gz`
3. Place in `DigitalDream/AI/Models/StableDiffusion/`

## Why separate repo?

The Unet model is ~1.6 GB, which exceeds the visionOS app bundle size limit of 4 GB. To solve this:

- Small models (TextEncoder, VAEDecoder, VAEEncoder) remain bundled in the app (~400 MB)
- Unet is downloaded on-demand from this repository on first use
- Total app bundle size: ~2.9 GB ✅

## License

Same license as the main Digital Dream app.
