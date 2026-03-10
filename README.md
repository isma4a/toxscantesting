 ToxiScan
Escaneá productos. Analizá ingredientes. Conocé lo que consumís.
ToxiScan es una aplicación web de archivo único (.html) que analiza ingredientes de alimentos, cosméticos y suplementos, asigna una puntuación de toxicidad y explica qué hay en cada producto.
No requiere instalación, servidor ni cuenta. Se abre directo en el navegador.

✨ Funcionalidades
📷 Escáner de barcodes

Cámara en vivo — apuntás al código de barras y lo lee automáticamente (requiere HTTP/HTTPS)
Foto — tomás una foto del barcode desde la cámara del teléfono, funciona incluso abriendo el archivo local
Entrada manual — escribís o pegás el número de barcode
Soporta EAN-13, EAN-8, UPC-A, UPC-E, Code 128, QR codes

🔬 Análisis de ingredientes

Pegás cualquier lista de ingredientes (separados por coma o línea) y obtener un análisis completo
Cada ingrediente recibe una puntuación de riesgo del 0 al 10
Muestra badges de tipo de riesgo: carcinógeno, disruptor endocrino, alérgeno, neurotóxina, etc.

🗄️ Buscador de ingredientes
El tab de ingredientes tiene tres modos:
Analyze List — análisis grupal de una lista completa
🔍 Search Ingredient — buscador individual:

Autocompletado instantáneo por nombre, número E o categoría
Ficha completa con descripción, nivel de riesgo, categoría y referencias regulatorias
Para suplementos: dosis típica, beneficios y advertencias
Botón para agregar directamente a la lista de análisis

📚 Browse DB — catálogo completo con 245+ ingredientes:

Filtros por categoría: Edulcorantes, Colorantes, Conservantes, Emulsionantes, Potenciadores de sabor, Grasas, Suplementos
Filtro de alto riesgo (≥ 7/10)
Ordenados por nivel de riesgo

🤖 Chat con IA

Asistente impulsado por Gemini con conocimiento especializado en ingredientes, aditivos, regulaciones FDA/EU e ingredientes de suplementos
Se activa desde el botón flotante en cualquier pantalla
Requiere clave de API gratuita de Gemini (ver configuración)

📋 Historial

Guarda los últimos 50 análisis automáticamente
Filtros por tipo: Alimentos, Cosméticos, Suplementos
Estadísticas de seguridad del historial


🗃️ Base de datos de ingredientes
La app incluye una base de datos propia con más de 245 ingredientes, dividida en dos partes:
ingredientsDB — Aditivos alimentarios, cosméticos y fármacos
Cubre más de 180 ingredientes incluyendo:

Conservantes — parabenos, nitritos, sulfitos, benzoatos, sorbatos, DMDM hidantoína
Colorantes artificiales — Red 40, Yellow 5, Yellow 6, Blue 1, Red 3, caramelo IV, tartrazina
Edulcorantes — aspartamo, sucralosa, sacarina, acesulfamo K, ciclamato, eritritol, xilitol, JMAF
Antioxidantes — BHA, BHT, TBHQ, vitamina E, ácido ascórbico
Emulsionantes y espesantes — carragenano, polisorbato 80, lecitina, CMC, pectina, goma xantana
Potenciadores de sabor — MSG, glutamato monosódico, disodio guanilato, proteína vegetal hidrolizada
Grasas — aceites parcialmente hidrogenados, aceite de palma, grasas interesterificadas
Agentes de tratamiento de harina — bromato de potasio, azodicarbonamida, harina blanqueada
Rellenos de suplementos — estearato de magnesio, dióxido de silicio, maltodextrina, dióxido de titanio
Colorantes naturales — annatto, beta-caroteno, carmín, curcumina

Cada entrada incluye: nivel de riesgo (0–10), lista de concerns, categoría, descripción con referencias regulatorias, y número E cuando aplica.
supplementsDB — Ingredientes de suplementos
Cubre más de 60 ingredientes de suplementos incluyendo:

Proteínas — whey aislado, caseína, proteína vegetal, colágeno
Performance — creatina monohidrato, beta-alanina, L-citrulina, HMB
Estimulantes — cafeína anhidra, DMAA ⚠️, DMHA ⚠️, sinefrina
Quemadores de grasa — yohimbina, extracto de té verde, garcinia cambogia
Aminoácidos — BCAA, L-glutamina, L-carnitina, L-teanina
Vitaminas y minerales — vitamina D3, magnesio glicinato, zinc, omega-3
Adaptógenos — ashwagandha, tongkat ali, tribulus terrestris
Nootropicos — lion's mane, alpha GPC, bacopa monnieri
Sustancias prohibidas — DMAA, SARMs, esteroides anabólicos, DNP

Cada suplemento incluye: nivel de riesgo, dosis típica, beneficios documentados y advertencias de seguridad.

🌐 APIs usadas para búsqueda de barcodes
Los barcodes se buscan en cascada, en este orden:

Open Food Facts — base de datos global de alimentos (openfoodfacts.org)
Open Beauty Facts — cosméticos y cuidado personal (openbeautyfacts.org)
Open Products Facts — suplementos y productos generales (openproductsfacts.org)
UPC Item DB — base de datos de productos UPC
Go-UPC — búsqueda de productos por código
Gemini AI — identificación por IA cuando no se encuentra en ninguna base de datos


⚙️ Configuración
Clave de API de Gemini (opcional pero recomendada)
La IA de Gemini habilita:

Identificación de productos por barcode cuando las otras APIs fallan
Chat asistente de ingredientes
Inferencia de ingredientes para productos desconocidos

Para obtener tu clave gratuita:

Entrá a aistudio.google.com
Hacé clic en "Get API Key"
Copiá la clave y pegála en Ajustes (⚙️) dentro de la app

🏷️ Sistema de puntuación
PuntuaciónGradoSignificado0–10AExcelente — ingredientes seguros11–25BBueno — bajo riesgo26–45CRegular — algunos ingredientes cuestionables46–65DMalo — ingredientes problemáticos66–100FMuy malo — ingredientes de alto riesgo
La puntuación se calcula en base al riesgo ponderado de cada ingrediente, con mayor peso para ingredientes con concerns de carcinogenicidad, toxicidad reproductiva y disrupción endocrina.

🛠️ Stack técnico

HTML / CSS / JavaScript puro — sin frameworks, sin build
Fuentes: Space Mono + DM Sans (Google Fonts)
Escáner: ZXing @zxing/library@0.19.1 + BarcodeDetector API nativa
IA: Google Gemini 2.0 Flash
Almacenamiento: localStorage (historial y ajustes)
Sin backend — todo corre en el navegador


📂 Archivos incluidos
index.html               ← La aplicación completa
README.md                      ← Este archivo

⚠️ Disclaimer
ToxiScan es una herramienta educativa e informativa. No reemplaza el consejo médico, nutricional ni farmacéutico profesional. Los niveles de riesgo son aproximaciones basadas en la literatura científica disponible y regulaciones internacionales. Consultá siempre a un profesional de salud ante dudas sobre ingredientes específicos.
