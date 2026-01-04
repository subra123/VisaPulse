# 💳 VisaPulse: The Active Benefit Intelligence Agent
### Transforming Static Credit Card Benefits into Real-Time Value

![Status](https://img.shields.io/badge/Status-Prototype-blue)
![Track](https://img.shields.io/badge/Track-Problem_Statement_2-green)
![Team](https://img.shields.io/badge/Team-BLUE-orange)
![Stack](https://img.shields.io/badge/AI-Google_Gemini-8E75B2)

---

## 🚀 The Problem

Nearly **70% of credit card benefits go unused** because they are hidden inside long PDFs written in legal and banking jargon. Users are unaware of what they are entitled to and do not know when or where to use their benefits—such as at airports, restaurants, or during shopping.

This results in:
- Missed savings and perks for users  
- Lower card engagement for banks  
- Untapped ecosystem value for payment networks  

The core gap is the **absence of real-time, context-aware benefit intelligence**.

---

## 💡 The Solution

**VisaPulse** is a **privacy-first, GenAI-powered benefit intelligence agent** that surfaces the *right benefit at the right moment*.

By combining **Visa product data**, **user context (location, time, profile)**, and **Generative AI**, VisaPulse transforms a static card number into an **active financial companion**—without storing or exposing sensitive card data.

---

## ✨ Key Features

- **🔒 Privacy-First Design**  
  No PAN or CVV is stored. Only BIN-based lookup (first 6–8 digits) is used to identify card products securely.

- **🧠 RAG-Powered Accuracy**  
  Retrieval-Augmented Generation ensures recommendations are grounded in actual benefit terms, avoiding hallucinations.

- **📍 Context-Aware Intelligence**  
  Recommendations dynamically adapt based on user location, time, and profile.

- **🗣️ Vernacular Support**  
  Complex financial benefits are translated into simple English or Tamil for better accessibility.

---

## 🛠️ System Architecture

The system is designed to be **PCI-DSS aware by design**, with strict separation between sensitive card data and AI processing.

```mermaid
graph LR
    A[User UI] -- Masked Card & Context --> B[Backend Orchestrator]
    B -- BIN Lookup --> C{Visa Product Database}
    C -- Raw Benefits --> D[RAG Engine]
    D -- Context + Benefits --> E[Google Gemini 1.5 Flash]
    E -- Personalized Output --> A
