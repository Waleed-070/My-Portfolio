# ROBOT-MOTHER Troubleshooting Guide

## Common Issues & Solutions

### Face and Head Problems

#### Issue: Distorted or Asymmetrical Face
**Symptoms:**
- Uneven eyes or crooked features
- Misaligned facial elements
- Unnatural proportions

**Solutions:**
1. **Lower CFG Scale:** Reduce from 8.0 to 7.0 or 6.5
2. **Add to Negative Prompt:** `asymmetrical face, distorted facial features, uneven eyes, crooked mouth`
3. **Use Face Restoration:** Enable in Automatic1111 or platform equivalent
4. **Change Sampler:** Try Euler a instead of DPM++ 2M Karras
5. **Reduce Step Count:** Too many steps can over-process faces

#### Issue: Looks Too Human or Organic
**Symptoms:**
- Skin appears biological, not synthetic
- Natural skin textures visible
- Android nature lost

**Solutions:**
1. **Strengthen Material Keywords:** `(polished chrome:1.3), (brushed aluminum:1.3)`
2. **Add Negative Terms:** `human skin, biological texture, flesh, pores, acne, blemishes`
3. **Emphasize Synthetic:** `synthetic materials, artificial, manufactured, precision engineered`
4. **Use Technical Models:** Switch to cyberpunk or sci-fi focused models

#### Issue: Face Too Dark or Poorly Lit
**Symptoms:**
- Facial features lost in shadow
- Circuit patterns not visible
- Flat, uninteresting lighting

**Solutions:**
1. **Add Lighting Keywords:** `cinematic lighting, volumetric lighting, rim lighting, soft shadows`
2. **Include Light Sources:** `bioluminescent glow, cyan magenta ambient light, holographic illumination`
3. **Camera Settings:** `shot on Arri Alexa, professional photography, cinematic lighting`
4. **Adjust Exposure:** Increase brightness in post-processing or regenerate with lighting emphasis

### Material and Texture Issues

#### Issue: Chrome Looks Like Plastic
**Symptoms:**
- Metal appears shiny plastic
- No realistic metallic reflections
- Toy-like appearance

**Solutions:**
1. **Metallic Emphasis:** `(metallic reflections:1.3), (chrome polish:1.3), brushed aluminum texture`
2. **Material Specifics:** `highly reflective, mirror finish, metallic surface, cold metal`
3. **Negative Terms:** `plastic, toy, mannequin, wax figure, cheap materials`
4. **Lighting Adjustment:** Add `specular highlights, realistic reflections`

#### Issue: Circuit Patterns Not Visible
**Symptoms:**
- Bioluminescent circuits missing
- No cyan/magenta glow
- Android details lost

**Solutions:**
1. **Circuit Emphasis:** `(bioluminescent circuits:1.3), (glowing patterns:1.2), cyan and magenta light`
2. **Technical Details:** `intricate circuit board traces, LED patterns, fiber optic illumination`
3. **Contrast Settings:** Increase contrast or add `high contrast, dramatic lighting`
4. **Layer Separation:** Use inpainting to enhance circuit areas

#### Issue: Hair Looks Fake or Unnatural
**Symptoms:**
- Fiber-optic effect not achieved
- Hair appears solid or plastic
- No data shimmer effect

**Solutions:**
1. **Fiber-Optic Specifics:** `(fiber-optic filaments:1.3), data streams in hair, shimmering with information`
2. **Movement Keywords:** `flowing, cascading, dynamic, animated`
3. **Technical Hair:** `synthetic hair strands, technological hair, cybernetic hair`
4. **Negative Terms:** `normal hair, human hair, biological hair`

### Background and Setting Issues

#### Issue: Background Overpowers Subject
**Symptoms:**
- Temple details too prominent
- Holographic elements distracting
- ROBOT-MOTHER gets lost in scene

**Solutions:**
1. **Depth of Field:** `shallow depth of field, bokeh, focus on subject`
2. **Background Blur:** `blurred background, soft focus background`
3. **Subject Emphasis:** `(ROBOT-MOTHER:1.3), portrait focus, main subject`
4. **Background Reduction:** Minimize background elements or add `subtle background`

#### Issue: Art Deco Elements Missing
**Symptoms:**
- No art deco aesthetics visible
- Purely futuristic design
- Lacks period fusion

**Solutions:**
1. **Art Deco Keywords:** `(art deco aesthetics:1.2), geometric patterns, streamlined design, elegant lines`
2. **Fusion Emphasis:** `art deco meets cybernetics, period futurism, retro-futuristic`
3. **Architectural Elements:** `art deco architecture, geometric motifs, symmetrical design`
4. **Historical Reference:** `1920s futurism, classic science fiction, vintage future`

### Color and Lighting Problems

#### Issue: Colors Oversaturated or Unnatural
**Symptoms:**
- Cyan/magenta too intense
- Skin tones unrealistic
- Color balance off

**Solutions:**
1. **Color Balance:** Add `natural colors, balanced saturation, realistic color palette`
2. **Camera Reference:** `shot on Arri Alexa, professional color grading, cinematic color science`
3. **Negative Terms:** `oversaturated, undersaturated, weird colors, color cast`
4. **Subtlety Keywords:** `subtle colors, muted tones, professional photography`

#### Issue: Lighting Flat or Uninteresting
**Symptoms:**
- No dramatic shadows
- Flat, uninteresting appearance
- Lacks cinematic quality

**Solutions:**
1. **Dramatic Lighting:** `dramatic lighting, volumetric lighting, cinematic atmosphere`
2. **Light Direction:** `side lighting, rim lighting, low angle lighting`
3. **Shadow Details:** `soft shadows, dramatic shadows, shadow depth`
4. **Professional Terms:** `professional lighting setup, studio lighting, cinema lighting`

### Technical and Platform Issues

#### Issue: Generation Takes Too Long
**Symptoms:**
- Excessive wait times
- Platform timeouts
- Resource exhaustion

**Solutions:**
1. **Reduce Resolution:** Start with 512x288, then upscale
2. **Lower Step Count:** Reduce from 50 to 30 steps
3. **Batch Management:** Generate 2 images instead of 4
4. **Platform Choice:** Switch to faster service for testing

#### Issue: Low Quality or Pixelated Results
**Symptoms:**
- Blurry or unclear images
- Compression artifacts
- Poor detail resolution

**Solutions:**
1. **Increase Steps:** Raise to 40-50 steps
2. **Higher Resolution:** Use 1024x576 instead of 768x432
3. **Quality Settings:** Enable highest quality options
4. **Upscaling:** Use platform upscaling or Hires. fix

#### Issue: Platform-Specific Problems

**Leonardo.ai:**
- **Credit exhaustion:** Use free tier strategically or upgrade
- **Inconsistent quality:** Try different models
- **Generation limits:** Use batch generation efficiently

**DreamStudio:**
- **Cost concerns:** Monitor credit usage
- **Slow processing:** Use queue during off-peak hours
- **Model limitations:** Experiment with different SD versions

**Automatic1111:**
- **Hardware issues:** Reduce batch size or resolution
- **Model problems:** Reinstall or update models
- **Memory errors:** Use `--lowvram` or `--medvram` flags

## Advanced Troubleshooting

### Complex Multi-Problem Issues

#### Issue: Multiple Quality Problems
**Systematic Approach:**
1. **Isolate Variables:** Test one change at a time
2. **Baseline Establishment:** Generate simple version first
3. **Incremental Addition:** Add complexity gradually
4. **Comparison Testing:** A/B test different solutions

#### Issue: Style Not Achieved
**Style Matching Strategy:**
1. **Reference Images:** Find similar style examples
2. **Style Keywords:** Extract and reuse effective terms
3. **Model Selection:** Try style-specific models
4. **Hybrid Approach:** Combine different prompts

### Recovery Strategies

#### When Everything Goes Wrong
**Reset Protocol:**
1. **Return to Master Prompt:** Strip to basic elements
2. **Default Settings:** Reset to platform defaults
3. **Simple Generation:** Generate basic android portrait
4. **Gradual Enhancement:** Add complexity back systematically

#### Prompt Corruption
**Prompt Cleanup:**
1. **Remove Special Characters:** Clean formatting
2. **Check for Conflicts:** Remove contradictory terms
3. **Length Optimization:** Shorten if too complex
4. **Syntax Correction:** Fix platform-specific syntax

## Prevention Strategies

### Pre-Generation Checks
- [ ] Prompt tested for conflicts
- [ ] Negative prompt comprehensive
- [ ] Settings appropriate for hardware
- [ ] Platform limits understood

### During Generation Monitoring
- [ ] Watch for early warning signs
- [ ] Stop problematic generations early
- [ ] Save intermediate results
- [ ] Document what works

### Post-Generation Learning
- [ ] Analyze successful generations
- [ ] Document failure patterns
- [ ] Update prompt library
- [ ] Refine workflow

## Quick Reference Solutions

| Problem | Immediate Fix | Long-term Solution |
|---------|----------------|-------------------|
| Face distortion | Lower CFG to 7.0 | Master face-specific prompts |
| Plastic look | Add metal emphasis | Use material-focused models |
| No circuits | Emphasize bioluminescent | Technical prompt library |
| Flat lighting | Add volumetric lighting | Lighting prompt variants |
| Slow generation | Reduce steps/resolution | Hardware/platform upgrade |

## Emergency Recovery

### Complete Failure Recovery
1. **Stop Generation:** Don't waste credits/time
2. **Simplify Prompt:** Return to basic elements only
3. **Reset Settings:** Use platform defaults
4. **Model Change:** Try different model
5. **Platform Switch:** Use alternative service

### Quality Emergency
When deadline approaching and quality not acceptable:
1. **Use Best Result:** Work with what you have
2. **Post-Process:** Enhance with editing software
3. **Composite Elements:** Combine best parts
4. **Professional Help:** Consider hiring editor

## Documentation for Future Prevention

### Issue Tracking Log
For each problem encountered, document:
- [ ] Problem description
- [ ] Platform used
- [ ] Prompt variations tried
- [ ] Solution that worked
- [ ] Prevention strategy

### Success Pattern Library
Maintain record of:
- [ ] Successful prompt combinations
- [ ] Effective settings
- [ ] Model preferences
- [ ] Platform advantages

This troubleshooting guide should resolve most common ROBOT-MOTHER generation issues and prevent future problems through systematic prevention strategies.