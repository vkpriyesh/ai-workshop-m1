## **3. Image Creator That Takes Image Details as Input and Appends JSON Prompt**

```json
{
  "task": "Generate a high-quality, photorealistic or stylized image based on the provided details",
  "input_details": {
    "subject": "Example: Lighthouse on a cliff overlooking the ocean at golden hour",
    "style": "Example: ultra-realistic, cinematic lighting, vibrant colors",
    "mood": "Example: calm, inspiring, adventurous",
    "size": "1024x1024",
    "color_palette": ["#FFD700", "#1E90FF", "#2E8B57"],
    "lighting": "Example: soft golden hour light, gentle shadows, lens flare"
  },
  "output_parameters": {
    "quality": "ultra high",
    "format": "webp",
    "negative_prompt": "no text, no watermarks, no human figures unless specified",
    "composition_notes": [
      "Strong focal point centered",
      "Balanced foreground and background",
      "Use depth of field for realism"
    ]
  },
  "post_processing": {
    "adjustments": ["brightness +5%", "contrast +10%", "sharpening for details"],
    "variants": 2
  }
}
```
