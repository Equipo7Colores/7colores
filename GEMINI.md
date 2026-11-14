# Contexto del Proyecto: Siete Colores — Equipo Terapéutico

Documento de instrucciones, contexto y bitácora técnica de desarrollo para Antigravity / Gemini CLI.

---

## 1. Descripción General
- **Cliente:** Siete Colores - Equipo Terapéutico.
- **Rubro:** Espacio interdisciplinario de salud, neurodesarrollo y clínica para infancias, jóvenes y adultos.
- **Sede Física:** Joaquín V. González 1061, Burzaco, Almirante Brown, Prov. de Buenos Aires.
- **Tecnología:** HTML5 semántico, CSS3 compilado (Tailwind tokens), JavaScript nativo (cero dependencias externas, sin CDNs pesados).
- **Despliegue Oficial en Vercel:** [https://7colores.vercel.app/](https://7colores.vercel.app/)
- **Repositorio Oficial en GitHub:** [https://github.com/Equipo7Colores/7colores.git](https://github.com/Equipo7Colores/7colores.git) (rama `main`).
- **Contacto Oficial Centralizado:** WhatsApp `+54 9 11 5796-7152` (`https://wa.me/5491157967152`).
- **Canal Oficial de YouTube:** [@equipo7colores](https://www.youtube.com/@equipo7colores) (`https://www.youtube.com/@equipo7colores`).
- **Atribución en Footer:** [GermyCode](https://germycode.com.ar).

---

## 2. Idioma y Reglas de Interacción
- **Idioma:** Responder siempre en **castellano / español**.
- **Entorno de ejecución:** Compatible tanto con Linux como con Windows.
- **Canalización de Consultas:** Todas las consultas y turnos del sitio se canalizan exclusivamente al número central oficial (`+54 9 11 5796-7152`). Las tarjetas profesionales no deben mostrar teléfonos particulares ni enlaces directos individuales.

---

## 3. Estructura de Archivos
- `index.html`: Landing page institucional completa (navegación híbrida desktop/app móvil, formulario de admisión a WhatsApp, schema.org `MedicalClinic`).
- `estilos.css`: Sistema de diseño con tokens CSS y utilidades base compiladas.
- `assets/`: Imágenes de alta calidad en WebP/JPG (fotos de profesionales, fachada, salas y OG image).
- `README.md`: Documentación interna del proyecto y guía de reemplazo de assets.
- `.gitignore`: Filtro de temporales y archivos de sistema.

---

## 4. Equipo Profesional Acreditado (`#equipo`)
1. **Lic. Adriana Griselda Rotela** — Directora Institucional / Terapista Ocupacional
   - MN 970 · MP 100802 · RNP 264977 · CUIT 27-23103863-4
2. **Lic. Mónica Susana Belottini** — Terapista Ocupacional / Estimulación Temprana
   - MN 1166 · MP 762 (Integración Sensorial, Floortime, CAA, Neurodesarrollo)
3. **Lic. Jimena Viviana Delmoral Juárez** — Licenciada en Psicología (UBA)
   - MP 74237 · RNP 340.721 · CUIT 27-31604364-5

---

## 5. Especialidades Habilitadas (`#especialidades`)
1. Terapia Ocupacional & Integración Sensorial
2. Psicopedagogía Clínica
3. Psicología Clínica (Infanto-Juvenil y Adultos)
4. Fonoaudiología & Comunicación (SAAC)
5. Psicomotricidad & Neurodesarrollo
6. Estimulación Temprana (0 a 3 años)
7. Actividad Física Adaptada & Salud Motriz
8. Habilidades Sociales & Grupos Terapéuticos
9. Apoyo a la Integración Escolar (DAI / APND)

---

## 6. Flujo de Publicación
Al realizar modificaciones en `/home/german/proyectos/sietecolores`:
```bash
git add .
git commit -m "Descripción clara del cambio"
git push origin main
```
Vercel compila y despliega en segundos en `https://7colores.vercel.app/`.
