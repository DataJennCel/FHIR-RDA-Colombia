🏥 FHIR RDA Colombia

Implementación de un Resumen de Atención (RDA) en estándar HL7 FHIR R4, ajustado al contexto colombiano según la Resolución 1888 de 2025.

📋 Contexto

El sistema de salud colombiano históricamente ha operado con historias clínicas fragmentadas imposibilitando la comunicación entre sistemas.
El estándar HL7 FHIR permite la comunicación de historias clínicas de diferentes sistemas de salud permitiendo intercambiar datos clinicos de manera sencilla y estructura con el obejtivo de mejorar la calidad de atención para el paciente y facilitando la atención de este por parte del personal de salud.
La Resolución 1888 de 2025 hace obligatoria esta implementación para todas las IPS, EPS y proveedores de software del país antes de abril de 2026, convirtiendo la interoperabilidad en un requisito operativo urgente para el sector.

🎯 Objetivo del repositorio

Demostrar la construcción paso a paso de un RDA en formato FHIR R4, desde los recursos básicos hasta un Bundle completo ajustado a los códigos y extensiones colombianas definidas por HL7 Colombia.

📁 Contenido

- fhir_basico.ipynb
  Construcción de los recursos FHIR fundamentales basado en pequeña atención paciente "Ana Torres": Patient, Encounter, Condition, MedicationStatement
- bundle_rda.ipynb
  Empaquetado de recursos en un Bundle RDA completo de fhir_basico.ipynb
- bundle_rda_ana_torres.json
  Bundle guardado en archivo json
- bundle_colombiano.ipynb
  Bundle ajustado al contexto colombiano: códigos CUPS, extensión de régimen de salud, URLs oficiales del Ministerio de Salud
- bundle_rda_colombiano.json
  Bundle RDA colombiano guardado en archivo json - valido según resolucion 1888 de 2025

🧩 Recursos FHIR implementados

- Patient — con identificador de la Registraduría y extensión de régimen de salud colombiano
- Encounter — con código CUPS colombiano y código de habilitación Supersalud
- Organization — IPS con código de habilitación
- Practitioner — médico con registro RETHUS
- Condition — diagnóstico con código CIE-10
- MedicationStatement — medicamento con código ATC, dosis y vía de administración

🇨🇴 Estándares colombianos utilizados

- HL7 FHIR R4 ---> Base técnica del RDA
- CIE-10 --------> Codificación de diagnósticos
- CUPS ----------> Codificación de procedimientos y tipo de consulta
- ATC (OMS)------> Codificación de medicamentos
- RETHUS --------> Registro del profesional de salud

💻 Tecnologías

- Python 3.x
- Jupyter Notebooks
- Librería json (nativa de Python)

👩‍⚕️ Autora

Jenniffer Celis
Médica con 10 años de experiencia clínica, con apuesta al healthtech. Conocimientos en Python, SQL, análisis de datos y creación de soluciones digitales en salud.

- 🌐 Portfolio: jenniffer-celis.netlify.app
- 💼 LinkedIn: linkedin.com/in/jenniffer-celis

📚 Referencias

- Guía de Implementación RDA — HL7 Colombia
- Resolución 1888 de 2025 — Ministerio de Salud Colombia
- HL7 FHIR R4 — Especificación oficial
