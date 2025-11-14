# ROBOT-MOTHER Negative Prompts Library

## Master Negative Prompt
**Use for most generations:**
```
cartoon, anime, painting, drawing, illustration, low quality, blurry, pixelated, distorted face, malformed hands, ugly, deformed, artificial skin, plastic, toy, mannequin, watermark, text, signature, grainy, noisy, oversaturated, undersaturated, bad anatomy, extra limbs, missing limbs, disfigured, poor details, low resolution, jpeg artifacts, compression artifacts, duplicate, morbid, mutilated, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, ugly, blurry, bad anatomy, disfigured, poorly drawn face, mutation, extra limb, ugly, poorly drawn hands, missing limb, floating limbs, disconnected limbs, malformed hands, out of frame, long neck, long body, extra fingers, fewer fingers, extra arms, fewer arms, extra legs, fewer legs
```

## Category-Specific Negatives

### Quality Control
**For maximum photorealism:**
```
cartoon, anime, 3d, render, cgi, painting, drawing, sketch, illustration, artwork, low quality, low resolution, pixelated, blurry, grainy, noisy, artifacts, jpeg compression, watermark, text, signature, logo, username
```

### Face & Anatomy
**Prevent facial distortions:**
```
distorted face, malformed face, asymmetrical face, ugly face, disfigured face, deformed eyes, crossed eyes, lazy eye, mismatched eyes, bad anatomy, poor anatomy, extra limbs, missing limbs, malformed hands, poorly drawn hands, extra fingers, fewer fingers
```

### Material & Texture
**Ensure proper android materials:**
```
plastic skin, rubber skin, toy material, mannequin, wax figure, glossy plastic, cheap materials, artificial looking, fake, prosthetic, costume, halloween mask, rubber mask, plastic surgery
```

### Lighting & Color
**Control lighting and color issues:**
```
oversaturated, undersaturated, bad lighting, flat lighting, harsh shadows, blown highlights, crushed blacks, color cast, weird colors, unnatural colors, poor contrast, bad white balance
```

### Composition & Framing
**Maintain proper composition:**
```
out of frame, cropped, cut off, partially visible, awkward pose, uncomfortable pose, stiff pose, unnatural pose, bad composition, poor framing, centered composition, boring composition
```

## Specific Issue Prevention

### Face Distortion Prevention
```
asymmetrical face, distorted facial features, uneven eyes, crooked mouth, misaligned features, facial asymmetry, deformed jaw, malformed nose, disproportionate features, bad face proportions
```

### Hand & Limb Issues
```
malformed hands, poorly drawn hands, extra fingers, missing fingers, fused fingers, webbed fingers, too many fingers, too few fingers, distorted hands, bad hands, ugly hands, disfigured hands
```

### Android-Specific Problems
```
human skin, organic texture, biological features, flesh, blood vessels, pores, acne, blemishes, wrinkles (unless aged), age spots, freckles, moles, scars (unless intentional)
```

### Background Distractions
```
busy background, cluttered background, distracting elements, text in background, people in background, unwanted objects, modern furniture, inappropriate architecture, wrong time period elements
```

## Technical Quality Negatives

### Image Quality
```
low quality, low resolution, pixelated, blurry, grainy, noisy, artifacts, jpeg artifacts, compression artifacts, banding, posterization, chromatic aberration, lens distortion, motion blur (unless intended)
```

### Photography Issues
```
bad photo, poor photography, amateur photo, snapshot, camera shake, bad focus, out of focus, shallow depth of field (unless intended), lens flare (unless intended), overexposed, underexposed
```

## Stylistic Negatives

### Avoid Non-Realistic Styles
```
cartoon, anime, manga, comic, illustration, painting, watercolor, oil painting, digital art, 3d render, cgi, video game, toy, figurine, statue, sculpture, abstract, surreal
```

### Prevent Wrong Art Styles
```
impressionism, expressionism, cubism, surrealism, pop art, minimalism (unless intended), abstract art, modern art, contemporary art (unless specified)
```

## Prompt Length Management

### Short Version (for platforms with limits)
```
cartoon, anime, painting, low quality, blurry, distorted face, malformed hands, ugly, deformed, watermark, text, signature
```

### Medium Version (balanced)
```
cartoon, anime, painting, drawing, illustration, low quality, blurry, pixelated, distorted face, malformed hands, ugly, deformed, plastic, toy, mannequin, watermark, text, signature
```

### Full Version (maximum control)
```
cartoon, anime, painting, drawing, illustration, low quality, low resolution, pixelated, blurry, grainy, noisy, artifacts, jpeg compression, watermark, text, signature, logo, username, distorted face, malformed face, asymmetrical face, ugly face, disfigured face, deformed eyes, crossed eyes, lazy eye, mismatched eyes, bad anatomy, poor anatomy, extra limbs, missing limbs, malformed hands, poorly drawn hands, extra fingers, fewer fingers, plastic skin, rubber skin, toy material, mannequin, wax figure, glossy plastic, cheap materials, artificial looking, fake, prosthetic, costume, oversaturated, undersaturated, bad lighting, flat lighting, harsh shadows, blown highlights, crushed blacks, color cast, weird colors, unnatural colors, poor contrast, bad white balance, out of frame, cropped, cut off, partially visible, awkward pose, uncomfortable pose, stiff pose, unnatural pose, bad composition, poor framing
```

## Platform-Specific Adaptations

### Stable Diffusion (full control)
Use the complete full version for maximum quality control.

### Midjourney (character limits)
```
--no cartoon, anime, painting, drawing, illustration, low quality, blurry, pixelated, distorted face, malformed hands, ugly, deformed, watermark, text, signature, plastic, toy, mannequin
```

### DALL-E 3 (natural language)
```
Avoid cartoon styles, anime, paintings, drawings, illustrations, low quality images, blurry photos, pixelated images, distorted faces, malformed hands, ugly appearances, deformed features, watermarks, text, signatures, plastic texture, toy appearance, mannequin-like quality.
```

## Iterative Refinement Approach

### First Pass - Basic Quality
Start with short/medium negative prompt to establish basic quality.

### Second Pass - Detail Enhancement
Add specific negatives based on initial results:
- Face issues → add face-specific negatives
- Hand problems → add hand-specific negatives
- Material concerns → add material-specific negatives

### Final Pass - Perfection
Use full negative prompt with any additional problem-specific terms discovered during generation.

## Common Negative Prompt Combinations

### Portrait Focus
```
distorted face, malformed face, asymmetrical face, bad anatomy, poorly drawn hands, extra fingers, missing fingers, ugly, deformed, disfigured
```

### Full Body Focus
```
bad anatomy, extra limbs, missing limbs, malformed hands, poorly drawn hands, awkward pose, unnatural pose, bad composition
```

### Material Emphasis
```
plastic skin, rubber skin, toy material, mannequin, wax figure, glossy plastic, cheap materials, artificial looking, fake
```

### Photorealism Priority
```
cartoon, anime, painting, drawing, illustration, 3d render, cgi, low quality, low resolution, pixelated, blurry, grainy, noisy
```

## Testing Your Negative Prompts

### Control Test
Generate the same image with:
1. No negative prompt
2. Short negative prompt
3. Medium negative prompt
4. Full negative prompt

Compare results to understand the impact of negative prompts on your specific ROBOT-MOTHER generation setup.

### Platform Testing
Test different negative prompt lengths/styles on your chosen platform to find the optimal balance between character limit and quality control.

## Troubleshooting Guide

### If Still Getting Cartoons
Add stronger style negatives:
```
--style raw --no cartoon, anime, comic, illustration --stylize 250
```

### If Face Still Distorted
Focus on face-specific negatives:
```
asymmetrical face, distorted facial features, uneven eyes, crooked mouth, misaligned features, facial asymmetry
```

### If Materials Look Wrong
Emphasize material negatives:
```
plastic skin, rubber skin, toy material, mannequin, wax figure, glossy plastic, cheap materials, artificial looking
```

## Negative Prompt Best Practices

1. **Start simple** - Begin with basic quality negatives
2. **Iterate gradually** - Add specific negatives based on results
3. **Platform awareness** - Adapt to character limits and syntax
4. **Test systematically** - Compare results with different negative prompts
5. **Document findings** - Keep notes of what works for your setup
6. **Balance is key** - Too many negatives can constrain creativity
7. **Update regularly** - Refine based on new generation issues