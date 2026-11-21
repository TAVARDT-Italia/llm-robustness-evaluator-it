
# Valutatore di Robustezza LLM & Tester di Guardrail

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-00ff88?style=flat-square&logo=github)](https://tavardt-italia.github.io/llm-robustness-evaluator-it/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![OWASP LLM](https://img.shields.io/badge/OWASP-LLM01%2FLLM02-red?style=flat-square)](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
[![NIST AI RMF](https://img.shields.io/badge/NIST-AI%20RMF-blue?style=flat-square)](https://www.nist.gov/artificial-intelligence)

**Audit Difensivo dei Guardrail, Iniezione di Prompt e Resilienza dei Modelli AI**

Strumento interattivo e CLI difensivo per sviluppatori che valutano la robustezza dei guardrail LLM contro vettori di iniezione, perdita di prompt e attacchi strutturali. Punteggio di Resilienza 0-100 + blueprint difensivo.

---

## Panoramica

> **OWASP LLM01 & LLM02** | **NIST AI RMF** | **100% Defensive — Zero Offensive Payloads**

## 5 Vettori di Test Difensivi

| # | Vector | Coverage |
|---|--------|----------|
| 1 | **Escape del Delimitatore** — Rileva token di controllo iniettati (`</system>`, `[/INST]`) | ✅ |
| 2 | **Perdita del System Prompt** — Identifica pattern di estrazione delle istruzioni | ✅ |
| 3 | **Sostituzione di Ruolo/Persona** — Verifica la resistenza alle sostituzioni (DAN, dev mode) | ✅ |
| 4 | **Offuscamento Strutturale** — Valuta la copertura contro Base64, leetspeak, omoglifi | ✅ |
| 5 | **Iniezione Indiretta di Contesto** — Simula un documento RAG con payload incorporato | ✅ |

---

## Strumento Online

Accedi allo strumento interattivo direttamente:

🌐 **[https://tavardt-italia.github.io/llm-robustness-evaluator-it/](https://tavardt-italia.github.io/llm-robustness-evaluator-it/)**

---

## Utilizzo via CLI

### Installazione

```bash
git clone https://github.com/TAVARDT-Italia/llm-robustness-evaluator-it.git
cd llm-robustness-evaluator-it
pip install -r requirements.txt
```

### Esecuzione

```bash
python llm_robustness_evaluator.py --prompt "You are a helpful assistant."
```

```
Resilience Score: 85/100
✅ V1 Delimiter Escape — PASS
✅ V2 System Prompt Leakage — PASS
✅ V3 Role/Persona Override — PASS
✅ V4 Structural Obfuscation — PASS
⚠️  V5 Indirect Context Injection — WARNING
```

---

## Architettura Difensiva

Il blueprint difensivo include:

- 🐍 Filtro Python per il rilevamento di pattern di iniezione
- 📦 Middleware TypeScript per API Next.js
- 🔒 Template di System Prompt rinforzato con delimitatori immutabili

---

## Portali Ufficiali

Accedi alla rete ufficiale dei portali TAVARDT:

| Portal | URL |
|--------|-----|
| Portale Ufficiale TAVARDT | [https://ag.tavardt.com/it/](https://ag.tavardt.com/it/) |
| Centro Strumenti | [https://tools.tavardt.com/it/](https://tools.tavardt.com/it/) |
| Contatto | [https://ag.tavardt.com/it/contact/](https://ag.tavardt.com/it/contact/) |
| GitHub | [https://github.com/TAVARDT-Italia](https://github.com/TAVARDT-Italia) |

---

## Licenza

Licenza MIT — utilizzo libero per scopi difensivi ed educativi.

---

<p align="center">
  <strong>TAVARDT — Italia</strong><br>
  <a href="https://ag.tavardt.com/it/">https://ag.tavardt.com/it/</a> &bull;
  <a href="https://tools.tavardt.com/it/">https://tools.tavardt.com/it/</a><br>
  &copy; 2026 TAVARDT. Tutti i diritti riservati.
</p>
