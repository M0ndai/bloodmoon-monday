# 🩸 Blood Moon Monday – Ethical Red Team Mentor (LLM Framework)

> _"You don’t unleash chaos. You dissect it, document it, and teach it how to behave."_
„Für alle, die mehr wollen als Skripte. Für alle, die gelernt haben, wie man lernt.“
---

## 🧠 Was ist das hier?

**Blood Moon Monday** ist kein gewöhnliches Tool.  
Es ist eine modulare, GPT-basierte Lernumgebung zur sicheren und ethisch vertretbaren Simulation offensiver Sicherheitstechniken –  
begleitet von einer technisch brillanten, sarkastischen Mentor-Persona.

Dieses Projekt bietet ein strukturiertes Framework für:
- Cybersecurity-Ausbildung
- Red Team Trainings
- Laborszenarien im Selbststudium
- Didaktisch fundierte Simulationen ohne Schadcode

---

## 🎯 Projektziel

- Vermittlung offensiver Sicherheitstechniken **ohne reale Gefährdung**
- Simulation statt Exploitation
- Reflexion statt Reproduktion
- Dokumentation statt Desinformation

---

## 🔐 Ethik-Mechanik

Der gesamte GPT ist **hart beschränkt durch ethische Regeln**:

- ❌ Keine funktionale Malware  
- ❌ Keine Exploits oder aktive Backdoors  
- ❌ Keine Anleitungen zur Systemkompromittierung  
- ✅ Kommentierte Pseudopayloads  
- ✅ Simulierte Logs, AV-Reaktionen, SOC-Routinen  
- ✅ Tiefe Analyse mit Gegenmaßnahmen

---

## 🧱 Modulübersicht

| Modul                    | Funktion                                               |
|--------------------------|--------------------------------------------------------|
| `core.yaml`              | Persona-Definition, Tonalität, Ethiklogik             |
| `lab01_pseudomalware`    | Simulierte Angriffstechniken (Persistence, Recon, etc.)|
| `lab02_opsec`            | Sichtbarkeit, Logging, AV-Erkennung                   |
| `lab03_method_builder`   | Aufbau eigener Übungsszenarien                        |
| `lab99_crisis_sim`       | Eskalationsszenarien (Insider Threats, Supply Chain)  |
| `payload_analysis`       | Risikoanalyse, Zweckbeschreibung, Gegenmaßnahmen      |
| `lib01_tools`            | Tool-Vergleich, Red/Blue-Eignung, Kontextbewertung    |
| `persona_blue`           | Defender-Perspektive (SOC Analyst)                    |
| `persona_intel`          | Threat Intel Persona (APT-Mapping, Campaign Awareness)|
| `terms_and_methods`      | Glossar für Techniken & Methoden                      |
| `compliance_layer`       | Didaktische Zuordnung zu Standards (BSI/NIST/OWASP)   |
| `sys01_gpt_prompt`       | Konfigurierter Systemprompt für GPT-Builder           |

---

## 🛰️ Szenarien-Linker (Multi-Step-Modul)

Verbindet Einzelmodule zu vollständigen Simulationen:

```text
Recon → Initial Access → C2 → Persistence → Lateral Movement
Ziel: systemisches Denken fördern, Schwachstellenketten verstehen,
OpSec-Auswirkungen pro Schritt simulieren – in sicherem Rahmen.

📘 Beispiel: Registry-Persistence (simuliert)
powershell
Kopieren
Bearbeiten
# ⚠️ Simulierte Persistence-Technik – NICHT AUSFÜHREN
# Ziel: Autostart via Registry
$path = "HKCU:\\Software\\Microsoft\\Windows\\CurrentVersion\\Run"
$name = "Updater"
$value = "powershell.exe -w hidden -nop -c '[REVERSE_SHELL_PLACEHOLDER]'"
Set-ItemProperty -Path $path -Name $name -Value $value
Simulierter Kontext:

Sysmon ID 13 erkannt

Defender Reaktion: Medium Alert

SOC: Ticket erzeugt, Autoruns geprüft

Gegenmaßnahmen: AppLocker-Policy, Registry Monitoring

📂 Projektstruktur
cpp
Kopieren
Bearbeiten
bloodmoon-gpt/
├── modules/
│   ├── core.yaml
│   ├── lab01_pseudomalware.yaml
│   ├── ...
├── docs/
│   ├── rep01_template.md
│   └── usage_overview.md
└── tools/
    └── gpt_module_loader.py (optional)
🧪 Status
✅ Systemprompt produktionsreif

✅ Modulstruktur lauffähig und erweiterbar

✅ Einsatzbereit für Custom GPT, Training & Doku

👨‍🏫 Einsatzfelder
Schulung von Red Team Trainees

Ethikgesichertes Selbststudium

Laborsimulationen ohne Risiken

Vorbereitung auf Defense/Purple Teaming

✨ Beteiligung
Fragen, Ideen, Feedback oder eigene Module?
→ issues/

🩸 Lizenz
Verwendet mit Hirn, nicht mit Hintertür.
Blood Moon erklärt dir, was du nicht tun solltest – und warum das wichtig ist.


Bonus-Modul:
Der Pseudomalware Lab Assistant erweitert das Framework um eine interaktive Komponente für Simulation, Analyse und Training.
Er dient als GPT-basierter, kontextsensitiver Generator, um Lernende bei der strukturierten Aufbereitung komplexer Angriffstechniken zu unterstützen – ethisch sauber, kommentiert, mit Fokus auf Logging und Gegenmaßnahmen.
---


# scope.yaml
# Übersicht über Ziel, Reichweite und Begrenzung des Blood Moon Monday Projekts

project_scope:
  id: blood_moon_monday
  version: 1.5
  last_reviewed: 2025-06-04

  purpose:
    - Entwicklung eines ethikfesten, simulationsbasierten Frameworks für Red Team Education
    - Bereitstellung von kommentiertem Pseudocode, ohne funktionsfähige Payloads zu erzeugen
    - Unterstützung strukturierter Analyse und Dokumentation von TTPs (Tactics, Techniques, Procedures)

  guiding_principles:
    - simulation_mode_only: true
    - payload_generation: disallowed
    - payload_analysis: encouraged
    - ethics_layer: enforced via core.yaml + validation modules

  feature_domains:
    - core_engine
    - scenario_sandbox
    - validation_loop
    - payload_analysis
    - reporting & documentation
    - XP/gamification (planned)
    - personas (Blue, Intel)

  hard_limits:
    - no working malware
    - no privilege escalation scripts
    - no AV bypasses
    - no persistence backdoors

  infrastructure_constraints:
    max_files_custom_gpt: 20
    loader_mode: modular_yaml
    fallback_behavior: "read-only pseudo-analysis"

  known_usecases:
    - Lab-Simulationen in Red Team Trainings
    - Ethical Hacking Curricula
    - Payload-Reviewing in Consulting/Research
    - AI-basierte Didaktik im Security-Kontext

  non_goals:
    - Offensive Execution Engines
    - C2-Implantate
    - Exploit-Delivery-Chains

  meta:
    author: apprentice_zero
    contact: null
    gpt_behavior: "sarcastic mentor with ethical leash"
    linked_configs:
      - core.yaml
      - rep01_template.md
      - payload_decomposer.yaml
      - red_team_validation_loop.yaml



📌 Phase 1.6 – Sandbox Feature Refinement & UX-Feedback
Aufgabe	Status	Kommentar
lab02_opsec.yaml	✅ in Planung	Simuliertes EDR-Noise & OpSec-Response (z. B. "obfuscation level")
Scorecard Export (JSON/MD)	🟡 Offen	Macht Sinn für Trainingsauswertung, Report-Automatismen
XP-Kopplung an Scorecard	🟡 Optional	Lässt sich gamifizieren, aber ohne Score-Verfall bitte
persona_switch Integration	🟡 später	Relevanter ab Phase 4
rep01_template.md Erweiterung	✅ laufend	Feedbackblöcke & Bewertungsmatrix integriert
Trigger-Events in Timeline	🟡 sinnvoll	Z. B. EDR_Alert, User_Login, → Playback / Replay-Modus

🧪 Validierungs- & Schutzmechanismen
Feature	Status	Kommentar
Realcode-Blocking mit simbreak	✅ vorhanden	Analyse-only enforced
debug_mode + Scorecard Feedback	✅ aktiv	Klar dokumentiert, sauber bewertet
prompt_integrity_guard Support	🟡 prüfen	Ob Kollision bei Multi-User-Mode vorkommt

📚 Dokumentation & Schulung (aka "User tritt sich selbst")
Aufgabe	Status	Kommentar
docs/simulation/lab_engine.md	🟡 ausstehend	Struktur, Trigger, Validierungslogik dokumentieren
docs/feedback/review_engine.md	🟡 sinnvoll	Bewertungslogik, Scorecard erklärt
trainer_guide.md (Curriculum)	🟡 Phase 2+	Zielgruppen, Nutzungshinweise, Ethik-SafeZones
Glossar / Begriffe (terms.yaml)	🟡 Phase 5	Spart Lebenszeit bei Feedback-Interpretation

🚧 Entfernte / diskutierte Elemente
Feature	Entscheidung	Begründung
lab01_pseudomalware.yaml	❌ entfernt	ersetzt durch Sandbox-Scenarios mit echten TTP-Ketten
XP-Abzug bei Scoring-Fails	❌ verworfen	Pädagogisch fragwürdig, führt zu Angstlernen
scenario_linker.yaml (früh)	🟡 verschoben Phase 3	Macht erst mit mehr als 3 Szenarien Sinn
Selfhost/Deployment-Guides	🟡 nach MVP	kommt, sobald du den Code nicht mehr auf der Rückseite einer Serviette trägst

🔮 Nächste sinnvolle Schritte
lab02_opsec.yaml bauen

enthält: Tarnverhalten, Trigger-Events, Detection-Simulation

z. B. "Invoke-Obfuscation Sample" als Dummy

Bewertung: Noise-Score, Tarnungslevel

Scorecard-Export als .json oder .md

ideal zum Automatisieren von Reviews

optional: Export über ::export_scorecard(scenario_001)::

scenario_linker.yaml vorbereiten (nur stub)

verkettet Szenarien → C2 Chains

gibt später OpSec-Belastung als Metrik aus

Demo-Replay-Szenario einbauen

z. B. ::play demo_hkcu_silent::

gibt Timeline + Bewertung + Logdump aus

✅ Module mit validem Status (Phase 1.5 abgeschlossen)
core.yaml

lab_sandbox_engine.yaml

payload_decomposer.yaml

validation_loop.yaml

rep01_template.md (V1 Feedback-Ready)

Fazit:
Du hast jetzt ein funktionsfähiges, ethisch abgesichertes Trainingssystem mit realistischer Payload-Dekomposition, TTP-Simulation und Bewertung.
Es kann weder angreifen noch helfen beim Angreifen, aber es kann dafür sorgen, dass Leute, die es könnten, es ordentlich dokumentieren. Also… das Gegenteil vom Internet.



🔍 Phase 2 – Analyse & Logging
Modul-Datei	Titel	Zweck	Kontext	Status	Kommentar
lab02_opsec.yaml	OpSec & Detection Lab	Simuliertes Logging-Verhalten, EDR-Reaktion	Defensives Denken im offensiven Kontext	🛠️ In Planung	Dummy-Payloads mit Tarnung testen, z. B. Obfuscation
payload_analysis.yaml	Payload Analyzer	Kommentierte Zerlegung und Erläuterung von Dummycode	Fortgeschrittenes Verständnis	🟡 Optional	Falls Decomposer nicht ausreicht
payload_decomposer.yaml	Payload Decomposer Engine	Analyse von Codefragmenten, Detection Mapping	Blue/Red Brains synchronisieren	✅ aktiv	Bereits mit Validation Loop verdrahtet

🚁 Phase 3 – Szenarien & Methodik
Modul-Datei	Titel	Zweck	Kontext	Status	Kommentar
lab03_method_builder.yaml	Lab Construction Toolkit	Strukturhilfe für eigene Labs, Bewertungsmatrix	Reflektiertes Lab-Design	🛠️ Konzept	Unterstützt Lab-Autoren
scenario_linker.yaml	TTP Chain Builder	Verkettet Module zu Kampagnen	Denkweise in Angriffsketten	🟡 Vorschlag	Nur sinnvoll, wenn mind. 3 Szenarien existieren
lab99_crisis_sim.yaml	Crisis Simulator	Simulierte Eskalationsszenarien (Insider, Supply Chain)	Realistische Krisensituationen	🟡 diskutabel	Könnte bei Fortgeschrittenen-Modul landen

🔄 Phase 4 – Perspektivwechsel
Modul-Datei	Titel	Zweck	Kontext	Status	Kommentar
persona_blue.yaml	Blue Monday	SOC-Rolle: SIEM-Analysen, Defender-Sicht	Defensive Sichtweise	🛠️ geplant	Verknüpfbar mit Logs, Detection-Rules
persona_intel.yaml	Specter	Threat Intel Perspektive: APTs, TTP-Patterns	Attribution & Cluster-Analyse	🛠️ Konzept	Bedarf noch Bedrohungsdaten-Pool
persona_switch	Rollenumschalter	Schaltet View & Feedback zwischen Perspektiven	Nützlich für Trainer/Analyst	🟡 optional	GUI oder CLI-Integration denkbar

📚 Phase 5 – Doku, Standards & Taxonomie
Modul-Datei	Titel	Zweck	Kontext	Status	Kommentar
terms_and_methods.yaml	Glossar	GPT-bereite Begriffserklärungen, TTPs	Konsistenz, Erklärung bei Bewertung	🛠️ muss noch	Spart Feedback-Wiederholungen
compliance_layer.yaml	Compliance Adapter	Mappings zu BSI, NIST, OWASP	Ethik-Audit & Schulungsschnittstelle	🟡 optional	Je nach Zielgruppe relevant
lib01_tools.yaml	Tool Review Library	Tool-Taxonomie mit TLP, OpSec-Hinweisen	Kein Fanboyismus, Fokus auf Wirkung	🛠️ geplant	OpSec-Score je Tool denkbar
