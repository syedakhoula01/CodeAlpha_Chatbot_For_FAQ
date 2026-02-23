# ✨ GlowSkin — Skincare FAQ Chatbot
### 🏢 CodeAlpha Internship Task | Developed by Khoula

---

## 📌 About the Project

GlowSkin is an AI-powered customer-support FAQ chatbot built as part of my internship at **CodeAlpha**. It allows users to ask questions about skincare products, routines, ingredients, and brand policies — and receive instant, accurate answers powered by **machine learning text similarity (TF-IDF + Cosine Similarity)**.

---

## 🚀 Features

- 💬 Answers 20+ skincare-related FAQs intelligently
- 🤖 Uses TF-IDF vectorization + cosine similarity to match questions
- 🔁 Provides a friendly fallback for unrecognized questions
- 🎨 Custom pink/rose-themed Gradio chat interface
- 📋 Pre-loaded example prompts for easy testing
- 🌐 Public URL sharing via `share=True`
- 📋 Copy-to-clipboard support for answers

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Python | Core programming language |
| scikit-learn | TF-IDF Vectorizer & Cosine Similarity |
| NumPy | Numerical operations |
| Gradio | Interactive web-based chat interface |

---

## ⚙️ How It Works

1. At startup, all 20 FAQ questions are vectorized using `TfidfVectorizer`
2. The user submits a question → it's transformed into the same vector space
3. Cosine similarity is computed between the user's vector and all FAQ vectors
4. The FAQ with the highest similarity score (above threshold `0.2`) is selected
5. The corresponding answer is returned — or a fallback message if no match is found

---

## 💬 FAQ Topics Covered

- 🧴 Products offered (cleansers, serums, moisturizers, sunscreens, etc.)
- 💧 Skin type solutions — dry, oily, sensitive, acne-prone
- 🐰 Product ethics — cruelty-free (Leaping Bunny certified), vegan options
- 🚫 Ingredients avoided (no parabens, sulfates, phthalates)
- 🌿 Basic and advanced skincare routines
- 📦 Shelf life, usage instructions, exfoliation frequency
- 🚚 Pricing, shipping (50+ countries), return policy
- 🛒 Where to buy, samples, customer service contact
- 🤰 Pregnancy safety guidance

---

## 📦 Installation & Setup

**1. Install Dependencies**
```bash
pip install gradio scikit-learn
```

**2. Run the App**
```bash
python glowskin_chatbot.py
```

**3. Open in Browser**
Gradio will display a local URL (e.g., `http://127.0.0.1:7860`).  
If `share=True` is set, a public URL is also generated — shareable with anyone!

---

## 📁 Project Structure
```
glowskin_chatbot.py
├── faqs dict            → 20 Q&A pairs
├── SkincareBot class    → TF-IDF model + get_answer()
├── chatbot_response()   → Gradio handler function
├── custom_css           → Pink-themed UI styles
└── demo.launch()        → Starts the Gradio app
```

---

## 🙋‍♀️ Author

**Khoula**  
Intern @ CodeAlpha  
📅 February 2026
