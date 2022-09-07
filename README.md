# Stable Diffusion Dockerfile for ROCm

Run Stable Diffusion on an AMD card, using [this method](https://www.youtube.com/watch?v=d_CgaHyA_n4).
Using webui provided by https://github.com/sd-webui/stable-diffusion-webui.

1. Obtain `sd-v1-4.ckpt` and put it in `rocm/model.ckpt`
2. Run `./build-rocm` to build the Docker image
3. Run `./run-rocm` to run a shell in the Docker container
4. (optional) [GFPGAN](https://github.com/TencentARC/GFPGAN/releases/download/v1.3.0/GFPGANv1.3.pth) in /dockerx/src/gfpgan/experiments/pretrained_models
5. (optional) [RealESRGAN_X4](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.1.0/RealESRGAN_x4plus.pth) and [RealESRGan_x4_anime](https://github.com/xinntao/Real-ESRGAN/releases/download/v0.2.2.4/RealESRGAN_x4plus_anime_6B.pth) in /dockerx/src/realesrgan/experiments/pretrained_models
6. Run webui: `python scripts/webui.py --optimized --esrgan-cpu`, visit `http://localhost:7860/` in a browser
