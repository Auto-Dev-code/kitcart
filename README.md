# 🥕 KitCart: Meal Logistics & Planning Engine

[cite_start]**KitCart** is a budget-focused meal-planning app that converts chef-style meal concepts into adjusted servings, constraint-safe ingredient lists, and printable prep workflows.

[cite_start]Unlike standard recipe apps, KitCart focuses on **execution**: providing the infrastructure (labels, prep sheets, reheating instructions) to make home cooking viable for busy households[cite: 2].

## 🏗️ Architecture

We use a **Monorepo** structure to house our distinct logic and presentation layers:

* **🧠 Backend (`/backend`):** Python **FastAPI**. [cite_start]Handles the "Combinatorial Recipe Engine" [cite: 5][cite_start], nutritional math, unit conversions, and PDF generation (WeasyPrint)[cite: 10].
* **✨ Frontend (`/frontend`):** **Next.js 14** (App Router) + **Shadcn UI**. [cite_start]Provides a warm, "kitchen-style" interface for planning and management[cite: 10].
* **🗄️ Database:** **Supabase** (PostgreSQL) for storing user preferences, ingredients, and templates.

## 🚀 Key Features

* **Combinatorial Recipe Generation:** Recipes are assembled dynamically from `RecipeTemplates` and `IngredientPools` based on what you have and what you can eat. [cite_start]No external API dependencies[cite: 9].
* [cite_start]**Printable Infrastructure:** Generates professional PDF prep sheets, FDA-style nutrition labels, and container labels for meal prep[cite: 7].
* [cite_start]**Diabetes-Friendly Mode:** Strict "Plate Method" filtering that validates glycemic load and nutritional thresholds[cite: 8].
* [cite_start]**Smart Shopping:** Consolidates ingredients and groups them by aisle[cite: 7].

## 🛠️ Quick Start (Codespaces)

Since this project is optimized for GitHub Codespaces:

1.  Open the repository in a new Codespace.
2.  **Backend Setup:**
    ```bash
    cd backend
    pip install -r requirements.txt
    uvicorn main:app --reload
    ```
3.  **Frontend Setup:**
    ```bash
    cd frontend
    npm install
    npm run dev
    ```

## 🛡️ License
[cite_start]Private / Proprietary (System-generated recipes and logic)[cite: 11].
