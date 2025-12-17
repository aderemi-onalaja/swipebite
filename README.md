🍽️ SwipeBite

Emoji-first global food discovery.  
Swipe → Learn → Explore.

Discover meals from cultures around the world through emoji-based cards — no menus, no photos, no overwhelm.

---

✨ Features

- 🍛 **Emoji-First Discovery**  
  Browse global dishes through clean, custom food emojis — designed for instant recognition.

- 👉 **Swipe Interaction**  
  Swipe right to like, left to skip. Simple, familiar, frictionless.

- 🌍 **Cultural Context**  
  Tap any emoji to reveal:
  - Dish name
  - Country / region
  - Cuisine

- 🤖 **Smart Feed**  
  The discovery feed adapts based on swipe behaviour, cuisine affinity, and ingredient patterns — while intentionally surfacing unfamiliar foods.

- 🏆 **Leaderboards**  
  See the most-liked foods globally and by region.

- 🧑‍🍳 **Community Submissions**  
  Users can submit foods they want to see — expanding the global food map over time.

---

🔁 Workflow

1. 📱 Open SwipeBite  
2. 🍽️ Swipe through emoji food cards  
3. 👆 Tap to learn the dish name & origin  
4. ❤️ Like / ⏭️ skip to personalise your feed  
5. 🌎 Explore trending foods via leaderboards  

---

🧠 Emoji Engine (High Level)

SwipeBite uses a **custom emoji generation system** rather than relying on standard Unicode emojis.

- 🎨 Emojis are AI-generated on demand
- 📐 Visual constraints enforce:
  - Rounded shapes
  - Soft gradients
  - Subtle depth
  - High clarity at small sizes
- 🔁 Assets are reviewed and regenerated until they meet quality standards

See `/docs/emoji-engine.md` for full details.

---

🚀 Roadmap

- 🍱 Cuisine-specific swipe decks
- 🥦 Dietary filters (vegan, halal, gluten-free)
- 📍 “Find near me” restaurant discovery
- 📖 Recipe links
- 🧭 Cultural story cards
- 🍂 Seasonal food collections
- 🔗 Social sharing
- 📊 Engagement-driven emoji refinement

---

🛠️ Tech Stack (Proposed)

- 🖥️ **Frontend:** React / Next.js  
- ⚙️ **Backend:** Node.js (Express) or FastAPI  
- 🤖 **AI / Image Generation:** Replicate (emoji-focused & SDXL models)  
- 🗂️ **Storage:** S3 / Cloudflare R2  
- 🌐 **CDN:** Cloudflare  
- 🔐 **Auth:** Firebase / Auth0 (future)

---

📁 Project Structure

swipebite/  
├── frontend/        # Web / mobile client  
├── backend/         # API & services  
├── models/          # AI model configs & prompt templates  
├── docs/            # Product, emoji engine & research docs  
│   ├── emoji-engine.md  
│   ├── emoji-acceptance-checklist.md  
│   └── global-food-discovery.md  
├── README.md  
├── RESEARCH.md  
└── LICENSE  

---

🤝 Contributing

Pull requests are welcome.  
For major changes, please open an issue first to discuss the proposal.

---

📜 License

See `LICENSE`.

© 2025 Aderemi Onalaja. All rights reserved.
