# 🏦 Banking Service Agent (Agentic Demo)

A lightweight **agentic banking assistant** demo that:
1) **Retrieves customer products** from a local SQLite DB using a Customer ID  
2) **Consults a policy document** to answer what the customer can/can’t do with those products  
3) Responds with safe, policy-aligned guidance

> This project is for learning/demo purposes only. Uses fictitious policies and sample data.

---

## ✨ Features

- **Tool 1 — Product Retrieval:** fetches customer products by `customer_id` from SQLite
- **Tool 2 — Policy Q&A:** reads a policy document and finds relevant sections to answer questions
- **Agent Loop:** decides which tool(s) to call, then generates a final answer
- **Safety:** refuses actions not allowed by policy; avoids hallucinating account operations

---

## 🧠 How it works (High-level)

1. User provides **Customer ID**
2. Agent calls `get_customer_products(customer_id)` (SQLite)
3. User asks questions about products (e.g., limits, eligibility, constraints)
4. Agent calls `search_policy(question, product_context)` (policy retrieval)
5. Agent generates a final response **grounded in the retrieved policy**

---

## 📦 Project Structure (example)


cat > README.md <<'EOF'
