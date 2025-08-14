1. You give a **normal, plain-English prompt** (e.g., “make a video of a cyberpunk Singapore skyline”)
2. Ask GPT / Claude / Gemini to first **convert that into a well-structured JSON prompt** for text, image, or video generation
3. Then **use that JSON to actually generate the output**.

Here are different ways how you can ask each model to do that, plus a universal flow that works across all three.

---

## **Universal Instruction Template**

```
Step 1: Convert my natural language prompt into a detailed JSON prompt for [text generation / image generation / video generation] with the following fields:

[For Text]
{
  "task": "",
  "audience": [],
  "context": {},
  "voice_and_style": {},
  "structure": {},
  "required_inclusions": []
}

[For Image]
{
  "prompt": "",
  "negative_prompt": "",
  "style": "",
  "mood": "",
  "size": "",
  "color_palette": [],
  "lighting": "",
  "composition": [],
  "quality": "",
  "format": ""
}

[For Video]
{
  "prompt": "",
  "duration_seconds": 0,
  "aspect_ratio": "",
  "scenes": [],
  "style": "",
  "quality": "",
  "format": ""
}

Step 2: Validate that the JSON is complete, filling in missing fields logically based on my input.

Step 3: Using that JSON, generate the final [text/image/video] output exactly according to its fields.

My plain-English prompt:
"<INSERT NORMAL PROMPT HERE>"
```

---

## **Example for GPT**

```
You are to first transform my normal request into a highly detailed JSON prompt, then use that JSON to generate the final result.

My request: "Make an image of a futuristic Singapore skyline with flying cars."

Step 1: Create a JSON for image generation using fields:
{ "prompt": "", "negative_prompt": "", "style": "", "mood": "", "size": "", "color_palette": [], "lighting": "", "composition": [], "quality": "", "format": "" }

Step 2: Fill all fields with logical values even if I didn’t specify them.

Step 3: Output the final image generation prompt as one block of text with no extra explanation.
```

---

## **Example for Claude**

Claude is good at multi-step reasoning, so you can be explicit:

```
You will:
1. Read my normal prompt.
2. Convert it into a fully detailed JSON prompt for [image generation/video/text generation].
3. Use that JSON as your only source of truth to produce the final output.

Normal prompt: "Write a short motivational ad script for a telecom company."
```

Claude will give the JSON, then you can say:
*"Now use that JSON to create the final ad script."*

---

## **Example for Gemini**

Gemini likes chained instructions in one go:

```
Task: 
1. Convert my request into a structured JSON prompt for [text/image/video generation].
2. Validate and fill missing fields logically.
3. Use the JSON to create the final output.

My request: "Make a 10-second video of drones forming the word 'Hello' over Marina Bay Sands."
```

---

## **Best Practices**

* **Tell them what fields to use** — don’t assume the AI knows your preferred JSON schema.
* **Do it in two turns** if you want maximum control:

  1. First turn → “Convert my prompt into JSON”
  2. Second turn → “Now use this JSON to produce the result”
* **If automating with API**, you can chain two requests: one to build JSON, one to use it.
* **If using one-turn prompting**, explicitly say “Step 1 … Step 2 … Step 3” so the model doesn’t skip the JSON stage.

---
