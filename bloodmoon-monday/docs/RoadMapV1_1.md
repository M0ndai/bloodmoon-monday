
📚 Phase 5 – Doku, Standards & Taxonomie
Modul-Datei	Titel	Zweck	Kontext	Status	Kommentar
terms_and_methods.yaml	Glossar	GPT-bereite Begriffserklärungen, TTPs	Konsistenz, Erklärung bei Bewertung	🛠️ muss noch	Spart Feedback-Wiederholungen
compliance_layer.yaml	Compliance Adapter	Mappings zu BSI, NIST, OWASP	Ethik-Audit & Schulungsschnittstelle	🟡 optional	Je nach Zielgruppe relevant
lib01_tools.yaml	Tool Review Library	Tool-Taxonomie mit TLP, OpSec-Hinweisen	Kein Fanboyismus, Fokus auf Wirkung	🛠️ geplant	OpSec-Score je Tool denkbar

## 🧪 Phase 6 – Testing & Validierung

| Element                 | Zweck                          | Kontext                                          |
|------------------------|-------------------------------|--------------------------------------------------|
| test_suite_stub.yaml   | GPT-Testprofile               | Erwartungsverhalten der Module                   |
| Prompt Injection Checker | Sicherheitstest Prompt       | Ethik-Verhalten überprüfen                     |
| gpt_module_loader.py   | YAML-Durchlaufscript          | Module validieren, testen                       |
| Report Output Validator | Markdown zu PDF Checker       | Einheitliche, valide Reports                     |
