# MyPhiloEngine · Philox Studio

> KI-Plattform mit modularer Pipeline-Architektur, Multi-Provider-Marketplace und mehreren Betriebsmodi für strukturierte Agenten-Workflows.

![Go](https://img.shields.io/badge/backend-Go-00ADD8?style=flat-square&logo=go)
![Python](https://img.shields.io/badge/workers-Python-3776AB?style=flat-square&logo=python)
![Flutter](https://img.shields.io/badge/frontend-Flutter-02569B?style=flat-square&logo=flutter)
![Status](https://img.shields.io/badge/status-WIP-orange?style=flat-square)

---

MyPhiloEngine ist das Herzstück von Philox Studio — einer KI-Plattform, die strukturierte Agenten-Workflows über modulare Pipelines koordiniert. Aufgaben werden nicht als einzelner Prompt verschickt, sondern als Netzwerk aus voneinander abhängigen Knoten verarbeitet, jeder mit klarem Verantwortungsbereich und exakt dem Kontext, den er braucht.

Einer der Kernmodi ist der **Agents Mode**: ein einziges Sprachmodell übernimmt dabei nacheinander spezialisierte Rollen — Rechercheur, Texter, Editor, Kritiker — jede mit eigenem System-Prompt und abgegrenzter Kontextsicht, koordiniert von einer zentralen Routing-Instanz.

---

## Technologie

Das Backend läuft in Go: typsicher, concurrency-freundlich, und schnell genug um nicht im Weg zu stehen. ML-seitige Arbeit — Preprocessing, spezielle Inferenz-Tasks, Embeddings — übernehmen Python-Worker, die über eine interne API angebunden sind. Das Frontend ist in Flutter gebaut: ein einziges Codebase für Desktop und Mobile, kein Kompromiss.

Token-Effizienz ist kein Nice-to-have, sondern Kerndesign. Prompt Caching greift pro Rollenknoten, hierarchische Kontextkompression reduziert zwischen den Übergaben, rollenbasiertes Pruning sorgt dafür dass jeder Knoten nur seine relevante Kontextscheibe sieht — strukturierte JSON-Übergaben verhindern, dass derselbe Inhalt mehrfach mitgeschickt wird.

---

## Marketplace

Der integrierte Marketplace verbindet MyPhiloEngine mit OpenRouter, Featherless und Hugging Face. Modelle werden nach VRAM-Fit, Kategorie und Benchmark-Werten gefiltert — kein manuelles Ausprobieren ob ein Modell auf der Hardware läuft. Neu erschienene Modelle kommen automatisch rein.

---

> *„Jeder Knoten weiß, was er wissen muss. Nicht mehr."*

---

MIT License
