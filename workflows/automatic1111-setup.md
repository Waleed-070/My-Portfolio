# Automatic1111 WebUI Setup for ROBOT-MOTHER

## Installation
1. **Download and Install:**
   ```bash
   git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git
   cd stable-diffusion-webui
   webui-user.sh  # Linux/Mac
   # or run webui-user.bat on Windows
   ```

2. **Launch WebUI:**
   - Open browser to `http://localhost:7860`
   - Wait for models to download (first run)

## Model Installation

### Download Recommended Models
1. **Realistic Vision v6.0:**
   - Download from CivitAI: [Realistic Vision v6.0](https://civitai.com/models/4201/realistic-vision-v60-b1)
   - Place in `stable-diffusion-webui/models/Stable-diffusion`

2. **Cyber Realistic:**
   - Download from CivitAI: [Cyber Realistic](https://civitai.com/models/13950/cyber-realistic)
   - Place in `stable-diffusion-webui/models/Stable-diffusion`

### Additional Required Models
- **VAE:** `vae-ft-mse-840000-ema-pruned.safetensors`
- **Upscalers:** `4x-UltraSharp`, `ESRGAN_4x`

## ROBOT-MOTHATER Generation Settings

### Tab 1: txt2img
**Prompt:**
```
cinematic portrait of ROBOT-MOTHER, serene female android, face sculpted from polished chrome and brushed aluminum, intricate bioluminescent circuit patterns glowing soft cyan and magenta light, translucent pearlescent synth-skin, hair made of flowing fiber-optic filaments shimmering with data, minimalist futuristic temple setting, holographic data streams floating geometric shapes, art deco aesthetics fused with cybernetics, hyper-detailed, insanely detailed, photorealistic, volumetric lighting, cinematic, 8k resolution, shot on Arri Alexa, professional photography, masterpiece, ultra-realistic
```

**Negative Prompt:**
```
cartoon, anime, painting, drawing, illustration, low quality, blurry, pixelated, distorted face, malformed hands, ugly, deformed, artificial skin, plastic, toy, mannequin, watermark, text, signature, grainy, noisy, oversaturated
```

**Settings:**
- **Sampling method:** DPM++ 2M Karras
- **Sampling steps:** 30
- **CFG Scale:** 7.5
- **Size:** 768x432 (16:9 aspect ratio)
- **Batch count:** 4
- **Batch size:** 1

### Tab 2: Hires. fix (Upscaling)
**Enable Hires. fix:** ✅

**Upscale by:** 2.0
**Upscaler:** Latent
**Hires steps:** 20
**Denoising strength:** 0.5
**Hires prompt:** (same as main prompt)

### Advanced Settings
- **Seed:** -1 (random) for variations
- **Script:** X/Y/Z plot for testing variations
- **Checkpoint:** Select your chosen model
- **VAE:** vae-ft-mse-840000-ema-pruned

## Generation Workflow

### Step 1: Initial Generation
1. Load settings above
2. Generate 4 images
3. Select best result

### Step 2: Hires. Fix Upscaling
1. Enable Hires. fix
2. Use settings above
3. Generate upscaled version

### Step 3: Inpainting Refinement
1. Send to inpaint tab
2. Mask areas needing improvement:
   - Face details
   - Circuit patterns
   - Hair strands
3. Lower denoising: 0.3-0.4
4. Generate refined version

### Step 4: Final Upscaling
1. Use Extras tab for final upscale
2. Upscaler: 4x-UltraSharp
3. Target resolution: 2048x1152 (8K quality)

## ControlNet Integration (Optional)

### Setup ControlNet
1. Install ControlNet extension
2. Download required models:
   - OpenPose
   - Canny
   - Depth

### Usage for ROBOT-MOTHER
1. **OpenPose:** Maintain consistent android pose
2. **Canny:** Define circuit pattern edges
3. **Depth:** Ensure proper 3D structure

## Quality Optimization Tips

### Face Enhancement
- Use `face restoration` in settings
- Enable `CodeFormer` for natural results
- Lower CFG if face distortion occurs

### Lighting Control
- Add `cinematic lighting`, `volumetric lighting` to prompt
- Use `soft shadows`, `subsurface scattering`
- Adjust denoising for lighting consistency

### Material Realism
- Emphasize `metallic reflections`, `chrome polish`
- Add `glowing circuits`, `bioluminescence`
- Include `subsurface scattering` for synth-skin

## Common Issues & Solutions

### Face Distortion
- Lower CFG scale to 6.5-7.0
- Add `beautiful detailed face` to prompt
- Use face restoration

### Poor Circuit Details
- Increase sampling steps to 40-50
- Use ControlNet with line art
- Inpaint specific areas

### Lighting Problems
- Try different samplers (Euler a for softer)
- Adjust `volumetric lighting` prompt weight
- Post-process with photo editing

## Keyboard Shortcuts
- **Ctrl+Enter:** Generate
- **Ctrl+S:** Save settings
- **Ctrl+L:** Load settings
- **Tab:** Switch between tabs

## Export Settings
Save your ROBOT-MOTHER generation settings:
1. Click `Save` button in txt2img
2. Name file `robot-mother-config.txt`
3. Share settings for reproducibility