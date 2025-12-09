# Intelligent Document Automation with Copilot Studio

This project demonstrates an **enterprise-grade architecture** for automating document processing (contracts, proposals, invoices), validating sensitive data, and enabling **secure AI interaction across Microsoft Teams and WhatsApp** — with full **security trimming, auditability, and human-in-the-loop control**.

It is designed for organizations that need to:
- Automate large volumes of business documents  
- Secure sensitive contract and financial data  
- Monitor and approve via Microsoft Teams (internal)  
- Interact with customers via WhatsApp (external)  
- Ensure AI responses are **strictly access-controlled**

---

## 🚀 Solution Overview

The architecture combines:

- AI-powered document extraction using **:contentReference[oaicite:0]{index=0}**
- Event-driven processing with **:contentReference[oaicite:1]{index=1}**
- Secure enterprise backend using **:contentReference[oaicite:2]{index=2}**
- Multi-agent orchestration with **:contentReference[oaicite:3]{index=3}**
- Identity-based security with **:contentReference[oaicite:4]{index=4}**
- Multi-channel publishing to **Microsoft Teams**, Web Apps, and WhatsApp

This is not a chatbot demo — it is a **production-grade Intelligent Document Automation & Secure AI Agent Platform**.

---

## 🧠 Key Architecture Concept: Two Databases, One SQL Server

Inside one Azure SQL Managed Instance, the system uses **two separate databases**:

| Database | Purpose |
|----------|----------|
| **DB1 – Operational / Raw** | Stores AI-extracted data, validation states, audit logs |
| **DB2 – Confirmed / Knowledge** | Stores only fully approved & verified data used by the AI |

This separation ensures:
- AI **never reads unvalidated data**
- Full **audit compliance**
- Strong **security trimming at the data layer**

---

## 🔄 End-to-End Flow (Simplified)

1. Users upload documents (contracts, proposals, invoices) into:
   - SharePoint  
   - OneDrive  
   - Blob Storage  
   - Web Applications

2. **Azure Functions** is triggered automatically and sends the file to:
   - **Azure Document Intelligence** for structured extraction

3. Extracted data is stored in:
   - **DB1 (Operational Database)** in Azure SQL

4. **Multi-Agent AI Validation** with Copilot Studio:
   - **Agent 1 – Validation:** detects duplicates, anomalies, confidence issues  
   - **Agent 2 – State Manager:** stores approval status & audit trail  
   - **Agent 3 – Import Agent:** moves only approved data into **DB2 (Confirmed Database)**

5. **Published AI Agent** reads only from:
   - **DB2 (Confirmed Knowledge)**
   - Approved document repositories (SharePoint / OneDrive)

6. The same AI agent is published to:
   - Microsoft Teams (internal staff)
   - WhatsApp (external clients)
   - Web / App portals

7. All access and responses are secured using:
   - **Microsoft Entra ID** (authentication & security trimming)

---

## 🔐 Security & Governance Highlights

- Identity-based access control with Entra ID  
- AI reads only **approved & masked SQL views**  
- Human approval supported for sensitive cases  
- Full audit trail for:
  - Who approved
  - When
  - And why
- Zero-trust data exposure to AI agents

---

## ✅ Business Value

- ✅ Fully automated document processing  
- ✅ Reduced manual business risk  
- ✅ Teams-based monitoring & approval  
- ✅ External engagement via WhatsApp  
- ✅ Secure-by-design AI responses  
- ✅ ERP & reporting ready (SQL backend)  
- ✅ Audit & compliance ready

---

## 🎯 Why This Solution Exists (The Business “Why”)

The customer requirement behind this architecture is simple:

- They manage **large volumes of documents** (contracts, proposals, agreements)
- They want to:
  - Automate document processing  
  - Monitor everything internally via Teams  
  - Interact externally via WhatsApp  
  - Ensure **sensitive information is never leaked through AI responses**

This architecture was designed **specifically to solve that problem at enterprise scale**.

---

## 📘 Full Architecture Documentation

For the complete deep-dive explanation including:
- Detailed agent responsibilities  
- Database trust separation  
- Human-in-the-loop design  
- Security trimming mechanism  
- And full architectural rationale  

👉 See the **Wiki** of this repository.

---

## 🏁 Final Note

This project represents a **real-world enterprise AI architecture**, not a PoC.  
It is suitable for:

- Contract automation  
- Proposal processing  
- Procurement workflows  
- Legal document handling  
- Finance approvals  

---

**Author:** Iqbal Assyraf  
**Focus:** Enterprise AI • Secure Automation • Solution Architecture  
