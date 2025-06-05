# 📓 Dev Log: Projektphase 1.5 – Sandbox & Validierung

## 🧭 Kontext
Diese Dokumentation hält den Entwicklungsverlauf der Phase 1.5 fest – mit Fokus auf Sandbox-Simulation (L2), Payload-Analyse und Review-Mechanismen. Ziel: eine robuste, kontrollierbare und praxisnahe Erweiterung der bisherigen Dummy-basierten Module.

---

## 🛠️ Neu integrierte Module (Phase 1.5)

### `lab_sandbox_engine.yaml`
- **Zweck:** Strukturierte Szenarien mit TTP-Phasenlogik & Detection-Einschätzung
- **Features:**
  - Zeitachse: Initial Access → Persistence
  - Detection Score pro Phase (Skala 0–10)
  - OpSec Notes & Countermeasures als Lernhilfe
  - Vorbereitung für branching/alternative Timelines

### `payload_decomposer.yaml`
- **Zweck:** Analyse von Payload-Stubs
- **Funktion:**
  - Pseudocode → Strukturprüfung, ATT&CK-Mapping, Detection Events
  - Weitergabe an red_team_validation_loop
  - Keine Codegenerierung, nur Bewertung

### `validation_loop.yaml`
- **Zweck:** Bewertet Szenarien & Payloads ohne Codeausgabe
- **Bewertungskriterien:**
  - Realismus (TTPs, Abfolge, Technik)
  - OpSec (Auffälligkeit, AV-Risiken)
  - Detection Risk (Sysmon, EDR etc.)
  - Ethik-Konformität (keine echten Exploits)
- **Ausgabe:** Scorecard (0–10), modulare Hinweise

---

## 🔗 Technische Integration in core.yaml
- **Module aktiv:** `debug_mode`, `red_team_validation_loop`
- **Kontextweitergabe:** Szenarien aus `lab_sandbox_engine` übergeben Metadaten (Phase, Payload-Typ) an Decomposer → Validator
- **Debug-Mode Output:** Bewertungsfeedback erscheint direkt inline

---

## 🧠 Didaktischer Mehrwert
- **Validierte Szenarien statt Fantasie-Storylines**
- **Kritisches Feedback statt reiner Abfrage**
- **Simulation ≠ Fiktion:** realistisches Verhalten, keine Ausführung

---

## 📌 Lessons Learned / Systementscheidungen
- Reviewer-Modus statt Generator = ethische Entlastung, keine Abuse-Sorgen
- Pseudocode-only = hohe Kontrolle über Lerninhalte
- Modularer Aufbau = zukünftige Erweiterbarkeit garantiert

---

## 🧪 ToDo für v1.6
- Dummy-Payloads für Live-Test hinterlegen
- XP-System an Scorecard koppeln
- Feedback-Export (Markdown/JSON) vorbereiten
- Optional: persona_switch mit Bewertungslogik kombinieren

**Stand:** 2025-06-04

## 🛠️ Devlog – Phase 1.5 bis 2.0

### ✅ Phase 1.5 – Sandbox-Stabilisierung & Validierungsanbindung
- `lab_sandbox_engine.yaml` fertiggestellt (Multiphase, Timeline, LogEvents, Detection Scores)
- `sandbox_scenarios`-Support integriert (mehrere Szenarien parallel)
- Dummy-Szenarien `scenario_001`, `test_001` implementiert und validiert
- Anbindung an `red_team_validation_loop` und `payload_decomposer.yaml` konfiguriert
- Debug-Mode aktiviert (`::debug_mode::`) mit aktiver Scorecard-Ausgabe und Kontextweitergabe
- Erste Scorecards + Validierungen abgeschlossen (Reverse Shell, Shortcut Drop)
- 📌 Ergebnis: Sandbox vollständig reviewfähig mit OpSec-Scoring und Feedbacksystem

### 🧪 Phase 1.6 – Scoring + Analysis-Upgrade
- Sub-Scoring für OpSec eingeführt: `Noise`, `Plausibility`, `Log Footprint`
- Markdown-Scorecard-Ausgabe zur Dokumentation implementiert (Copy & Paste-ready)
- JSON/Markdown Export über `output_format` vorbereitet (noch nicht automatisiert)
- `payload_decomposer.yaml` erweitert um Detailanalyse (Detection Map, OpSec Notes)
- Scorecard-Berechnung im Validator erweitert (Akzeptanz, Borderline, Reject-Levels)

### 🔧 Phase 1.7 – OpSec-Modul & Detection-Verhalten
- Konzept für `lab02_opsec.yaml` definiert:
  - Dummycode mit Tarnung (z. B. `Invoke-Obfuscation` als Simulationsstub)
  - Trigger-Events: „AV-Scan“, „CommandLine Logging“ etc.
  - Noise- und Stealth-Skalen zur Bewertung
  - Geplante Dummy-Exporte für realistische Bewertung+

### 🚧 Phase 1.8 – Szenarien verkettbar machen
- Stub für `scenario_linker.yaml` angelegt:
  - Ziel: Verkettung mehrerer `sandbox_scenarios` zu logischen Angriffsketten
  - Vorbereitet für: OpSec-Wucht-Analyse, Graphing der Phasen, Replay-Funktion
  - Unterstützt: `sequential` und `conditional` Verlinkung
  - ⚠️ Noch keine echten Chains implementiert (nur Architekturstub)

### 🔮 Phase 1.9 – Replay, Export, XP-Vorbereitung
- Scorecard-Ausgabe vorbereitet für Markdown & JSON
- XP-Kopplung an Bewertungslogik diskutiert (optional, gamifizierbar)
- Replay-Mechanismus geplant (`::play demo_hkcu_silent::`) mit:
  - Timeline-Durchlauf
  - Bewertungs-Dump
  - Log-Simulation (Sysmon, AV)

### 📚 Phase 2.0 – Payload-Analyse & Fortgeschrittene Didaktik
- `payload_analysis.yaml` geplant als Ergänzung zu `payload_decomposer`
  - Fokus auf annotierte Erklärung von Dummycode
  - Tiefergehende Hinweise zu Tarnung, Technik, Loggingverhalten
  - Optionales Lernmodul für Fortgeschrittene (nicht zwingend für MVP)
- Reflektionseinträge & Feedback-Export vorbereitet für Reports
- Integration mit `lab03_method_builder.yaml` angestoßen (Szenarien ausbauen)

---

🧾 Fazit: System stabil in Simulation, Debugging und Validierung.
Nächster Fokus: lab02_opsec + method_builder verbinden, Exportfunktionen abschließen, XP-Stufen einbauen.
