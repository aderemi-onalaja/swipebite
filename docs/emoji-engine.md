# Emoji Engine — iOS-Inspired Emoji Generation System

This document describes the **Emoji Engine** used by SwipeBite to generate consistent, emoji-style food assets at scale.

The goal is to produce **emoji-first visuals** that feel familiar, friendly, and platform-native, while remaining legally distinct from any proprietary emoji sets.

---

## 🎯 Design Goal

Generate food emojis that:
- Feel **iOS-esque** (modern, soft, friendly)
- Are **clear and recognisable at small sizes**
- Maintain **visual consistency** across cuisines
- Can scale beyond Unicode emoji limitations
- Are generated programmatically via API

---

## 🧠 Core Principle

> **The Emoji Engine is defined by constraints, not the model.**

Models are interchangeable.  
The **visual spec + acceptance loop** is what creates consistency.

---

## 🧱 System Architecture (High-Level)

Food added (system or user)
↓
Food metadata validated
↓
Emoji prompt constructed (server-side)
↓
Image generated via model API
↓
Post-generation QA checks
↓
Accepted → stored & served
Rejected → regenerated

Frontend never controls prompts or generation.

---

## 🎨 Visual Specification (Locked)

All emojis must conform to the following spec.

### Canvas
- Square aspect ratio
- Transparent background
- Emoji-safe padding

### Perspective
- Slight 3/4 or top-down view
- No extreme angles

### Lighting
- Single soft light source
- Top-left or neutral
- No harsh shadows

### Shading
- Smooth gradients
- Soft transitions
- No flat fills
- No sharp shadow edges

### Shape Language
- Rounded
- Friendly
- Simplified
- No sharp or aggressive geometry

### Colour
- Natural food colours
- Slightly saturated
- No neon or artificial hues

### Detail Level
- Instantly readable at 64×64
- No micro-textures
- No clutter

### Exclusions
- No text
- No plates or utensils (unless culturally essential)
- No backgrounds
- No photorealism

---

## 🧩 Prompt Construction Strategy

Prompts are:
- Deterministic
- Repetitive
- Boring by design

Creativity is intentionally constrained.

### Example Prompt Template

Create a clean, friendly food emoji representing {{DISH_NAME}}.

Style rules:
	•	Rounded shapes
	•	Soft gradient shading
	•	Subtle depth
	•	Neutral, soft lighting
	•	Transparent background
	•	Clear and recognisable at small sizes

Do not include text, backgrounds, or unnecessary props.

---

## ⚓ Style Anchors (Convergence Mechanism)

A curated set of **approved emojis** is maintained internally as *style anchors*.

These anchors define:
- Lighting behaviour
- Depth
- Simplification level
- Colour balance

New generations are evaluated against these anchors to ensure convergence.

No proprietary emoji assets are used.

---

## 🔁 Regeneration Strategy

Emoji generation is **iterative by design**.

Triggers for regeneration:
- Fails acceptance checklist
- Low engagement (below swipe threshold)
- Updated visual spec version
- Improved model availability

---

## 📦 Asset Storage

Accepted emojis are:
- Stored in object storage (e.g. S3 / R2)
- Served via CDN
- Versioned by `emoji_spec_version`

Frontend consumes emojis as static assets.

---

## 🧠 Why This Approach

- Scales globally
- Avoids IP risk
- Supports continuous improvement
- Mirrors how real design systems evolve

The Emoji Engine is a **system**, not a prompt.
