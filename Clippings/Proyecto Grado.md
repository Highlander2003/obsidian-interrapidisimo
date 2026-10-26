---
title: proyecto Grado
source: https://app.murfy.ai/project/3019a510-a6cc-4cda-9476-8fd5a7051644?fileId=54627ab7-8cce-4ac5-b4d8-6f96ebe85511
author: Luis Fernando Caicedo - Sebastián Salazar Caicedo
published:
created: 2026-10-24
description: Write, review, and publish together — with AI. A modern Overleaf alternative with unlimited collaborators, AI-powered writing, and real-time collaboration.
tags:
  - clippings
---
Selection deleted

\\documentclass\[12pt,letterpaper,oneside\]{report}

% ---------- Idioma y fuente ----------

\\usepackage\[T1\]{fontenc}

\\usepackage\[english,spanish,es-noshorthands,es-tabla,es-nolists\]{babel}

\\usepackage{newtxtext} % Times New Roman 12 (exigida por la UNIAJC)

\\usepackage{textcomp}

\\usepackage{csquotes}

% ---------- Página: márgenes de 2,54 cm en los cuatro lados ----------

\\usepackage\[letterpaper,margin=2.54cm,headheight=15pt,headsep=0.75cm\]{geometry}

% ---------- Interlineado doble y sangría de 1,27 cm ----------

\\usepackage{setspace}

\\doublespacing

\\setlength{\\parindent}{1.27cm}

\\setlength{\\parskip}{0pt} % sin espacio adicional entre párrafos

\\usepackage{indentfirst} % sangría también en el primer párrafo de cada sección

% ---------- Paquetes generales ----------

\\usepackage{graphicx}

\\graphicspath{{img/}}

\\usepackage{xcolor}

\\usepackage{array,booktabs,tabularx,xltabular}

\\usepackage{float}

\\usepackage{enumitem}

\\setlist{nosep,leftmargin=1.27cm}

% ---------- Cornisa (encabezado) ----------

% La UNIAJC pide un resumen del título de máximo 50 caracteres, en mayúscula

% sostenida, alineado a la izquierda y con el número de página a la derecha.

\\newcommand{\\cornisa}{APLICACIÓN WEB PARA EL DESPACHO EN MENSAJERÍA}

\\usepackage{fancyhdr}

\\fancypagestyle{apa}{%

\\fancyhf{}%

\\fancyhead\[L\]{\\cornisa}%

\\fancyhead\[R\]{\\thepage}%

\\renewcommand{\\headrulewidth}{0pt}%

}

\\fancypagestyle{plain}{% también en las páginas donde inicia un capítulo

\\fancyhf{}%

\\fancyhead\[L\]{\\cornisa}%

\\fancyhead\[R\]{\\thepage}%

\\renewcommand{\\headrulewidth}{0pt}%

}

\\pagestyle{apa}

% ---------- Títulos según los niveles de APA 7 ----------

% Nivel 1 (capítulos): centrado y en negrita

- /74
- 106%

APLICACIÓN WEB PARA EL DESPACHO EN MENSAJERÍA 1 Aplicación web para la gestión del despacho en mensajería. Sistema de información para la  
gestión y trazabilidad del despacho de última milla: caso de referencia sucursal Inter  
Rapidísimo, Jamundí Luis Fernando Caicedo Sánchez  
Sebastián Salazar Caicedo  
Trabajo de grado para optar el título de Ingeniero de Sistemas  
Director \[Por completar: nombre del director\]  
\[Título académico más alto\] Institución Universitaria Antonio José Camacho  
Facultad de Ingenierías  
Ingeniería de Sistemas  
2026

APLICACIÓN WEB PARA EL DESPACHO EN MENSAJERÍA 2 Contenido Pág.  
1.Introducción.........................................10  
1.1 Planteamiento del problema..............................12  
1.1.1 Pregunta de investigación...........................14  
1.2 Justificación......................................14  
1.3 Objetivos.......................................17  
1.3.1 Objetivo general................................17  
1.3.2 Objetivos específicos.............................17  
1.4 Alcance........................................17  
1.5 Limitaciones......................................18  
2.Marco referencial......................................20  
2.1 Marco Teórico.....................................20  
2.1.1 El sector de la mensajería en Colombia y la importancia de la última milla.20  
2.1.2 Ingeniería de sistemas y enfoque sistémico..................21  
2.1.3 Gestión por procesos y notación BPMN 2.0.................21  
2.1.4 Sistemas de información logística y automatización de procesos......22  
2.1.5 Metodologías de desarrollo ágil: el modelo RAD..............23  
2.1.6 Fundamentos tecnológicos para el desarrollo web..............24  
2.1.7 Identificación automática por código de barras................25  
2.1.8 Trazabilidad y pistas de auditoría.......................26  
2.1.9 Arquitectura empresarial por capas......................26  
2.1.10 Seguridad en aplicaciones web........................27  
2.1.11 Continuidad operativa: objetivos de recuperación..............27  
2.1.12 Calidad del producto software: la norma ISO/IEC 25010..........27  
2.1.13 Evaluación económica de una intervención de mejora............28  
2.2 Marco Conceptual...................................28  
2.3 Marco Histórico y Antecedentes...........................31  
2.4 Marco Legal......................................32