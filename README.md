# Kableo ⚡💨🤖

**Kableo** web-nabigatzailean exekutatzen den eskema elektrikoen, neumatiakoen, elektronikakoen eta PLC (Ladder/KOP) programazioaren editore eta simulatzaile interaktiboa da. Irakaskuntzarako zein prototipo azkarrak egiteko pentsatua, instalaziorik gabe edozein gailutatik erabil daiteke.

*(Más abajo disponible en español / Available in Spanish below)*

---

## 🇪🇺 Euskara

### Ezaugarri nagusiak

* **⚡ Motor elektriko errealista (50 Hz-ko fasoreak):**
  * Ez da simulazio logiko huts bat: zenbaki konplexuen eta sistema linealen ebazpenaren bidez tentsioak eta fase-desfaseak kalkulatzen ditu.
  * Sistema trifasikoen ($L1, L2, L3, N, PE$) portaera fisikoa: biraketa-noranzkoaren aldaketa, fase-falta, izar/triangelu abioa, transformadoreak eta zirkuitulaburren detekzioa.
  * Kableatuaren kolore-kodearen egiaztapena eta iradokizun automatikoa.
* **🔌 Kableatu adimenduna:**
  * Eroale bakarra edo kable anitzak aldi berean marrazteko aukera (2tik 5era: trifasikoa + neutroa + lurra), bide mailakatuekin zirkuitulaburrak saihesteko.
  * Kableen tarteak perpendikularki arrastatzeko aukera, T formako loturak eta borneak galdu gabe.
  * Kable bakoitzaren sekzioa ($\text{mm}^2$) definitzeko eta etiketak esleitzeko aukera.
* **🔍 Simulazio aurreko akatsen berrikuspena:**
  * Planoa automatikoki aztertzen du: airean dauden borneak, bobinarik gabeko kontaktuak, marka bikoiztuak, zirkuitulabur zuzenak eta falta diren elikatze-iturriak.
  * Abisuan klik eginda kamerak zuzenean akatsaren puntura eramaten zaitu.
* **📏 Polimetro / Zunda birtuala:**
  * Simulazioan zehar edozein borne edo kableren gainetik sagua pasatzean tentsioa edo presioa neurtzen du.
  * Klik batekin erreferentzia-puntu bat finkatzen du tentsio-diferentziak ($\Delta V$) neurtzeko.
* **💨 Neumatiaka eta Elektroneumatika:**
  * Aire konprimituaren zirkuituen simulazioa: konpresoreak, mantentze-unitateak, 3/2, 5/2 eta 5/3 balbulak (monoestableak, biestableak, pilotatuak), emari-erregulatzaileak, ate logikoak (ETA/EDO) eta karrera-amaiera mekanikoak zein magnetikoak.
* **🔋 Elektronika eta Erdieroaleak:**
  * Diodoak, LEDak, artezgailu-zubiak, kondentsadoreak, NPN transistoreak eta egoera solidoko erreleak (SSR).
  * Gehiegizko korronte edo potentziagatik osagaiak erretzeko simulazioa eta bobinetan itzulera-diodoen egiaztapena.
* **🤖 PLC Editorea (Ladder / KOP):**
  * PLC modulua zirkuitu elektrikoarekin zuzenean lotuta: sarrera fisikoak (`I0.0`...) eta irteerak (`Q0.0`...), markak (`M0.0`...), tenporizadoreak (`TON`, `TOF`) eta kontagailuak (`CTU`).
* **📑 Orri anitzeko proiektuak eta erreferentzia gurutzatuak:**
  * Proiektu berean hainbat orri sortzeko aukera, orrien arteko konektoreekin eta bobina-kontaktuen arteko erreferentzia gurutzatuekin.
* **☁️ Hodeia eta Esportazioa:**
  * Proiektuak lokalean (`.json`) gordetzeko edo hodeian (Firebase bidez) sinkronizatzeko eta partekatzeko aukera.
  * Irudi gisa (PNG / SVG) eta materialen zerrenda (BOM) esportatzeko prest.

### Erabilera eta Laster-teklak

| Ekintza | Laster-tekla |
| :--- | :--- |
| **Osagaiak bilatu** | `Ctrl + K` |
| **Kablea marraztu / Hautatu** | `W` / `Esc` |
| **Osagaia biratu / Ispilatu** | `R` / `F` |
| **Simulazioa hasi / gelditu** | `F5` edo `Zuriunea` |
| **Desegin / Berregin** | `Ctrl + Z` / `Ctrl + Y` |
| **Kopiatu / Itsatsi** | `Ctrl + C` / `Ctrl + V` |
| **Planoan mugitu / Zooma** | `Erdiko botoia` / `Saguaren gurpila` |

### Instalazioa eta Exekuzioa

Aplikazioa **fitxategi bakarreko arkitekturan** dago garatuta (HTML/CSS/JS purua, kanpoko menpekotasunik gabe):

1. Deskargatu biltegi hau edo klonatu:
   ```bash
   git clone https://github.com/erabiltzailea/kableo.git
   ```
2. Ireki `index.html` fitxategia edozein web-nabigatzaile modernotan (Chrome, Firefox, Edge, Safari).
3. *(Aukerakoa)* Hodeiko funtzioak erabiltzeko, konfiguratu zure Firebase proiektuaren kredentzialak kodean.

---

## 🇪🇸 Castellano

### Características principales

* **⚡ Motor eléctrico realista (fasores a 50 Hz):**
  * No es una simple simulación lógica: resuelve circuitos mediante números complejos y sistemas lineales para calcular tensiones reales y desfases.
  * Comportamiento físico en sistemas trifásicos ($L1, L2, L3, N, PE$): inversión de giro, falta de fase, arranque estrella/triángulo, transformadores y detección de cortocircuitos.
  * Sugerencia y verificación automática del código de colores normalizado en los conductores.
* **🔌 Cableado inteligente:**
  * Trazado de conductores individuales o múltiples simultáneamente (de 2 a 5 hilos: trifásico + neutro + tierra), con rutas escalonadas para evitar cortocircuitos.
  * Arrastre perpendicular de tramos de cable manteniendo conectadas las derivaciones en T y los bornes.
  * Asignación de sección ($\text{mm}^2$) y etiquetas por conductor.
* **🔍 Revisión automática previa a la simulación:**
  * Analiza el esquema en tiempo real para detectar bornes al aire, contactos sin bobina asociada, etiquetas duplicadas, cortocircuitos directos o falta de alimentación.
  * Hacer clic en un aviso centra la cámara directamente en el error.
* **📏 Polímetro / Sonda virtual:**
  * Durante la simulación, al pasar el cursor sobre cualquier borne o cable muestra la tensión o presión instantánea.
  * Permite fijar un punto de referencia con un clic para medir diferencias de potencial ($\Delta V$).
* **💨 Neumática y Electroneumática:**
  * Simulación de circuitos de aire comprimido: compresores, unidades de mantenimiento, válvulas 3/2, 5/2 y 5/3 (monoestables, biestables, pilotadas), reguladores de caudal, válvulas selectoras/simultaneidad (O/Y) y finales de carrera mecánicos y magnéticos.
* **🔋 Electrónica y Semiconductores:**
  * Diodos, LEDs, puentes rectificadores, condensadores, transistores NPN y relés de estado sólido (SSR).
  * Simulación de destrucción térmica por sobrecorriente o exceso de potencia y aviso por falta de diodo de libre circulación en bobinas de CC.
* **🤖 Editor PLC (Ladder / KOP):**
  * Módulo PLC integrado en el esquema eléctrico con entradas físicas (`I0.0`...), salidas (`Q0.0`...), marcas (`M0.0`...), temporizadores (`TON`, `TOF`) y contadores (`CTU`).
* **📑 Proyectos multi-hoja y referencias cruzadas:**
  * Gestión de múltiples hojas dentro de un mismo libro con conectores entre páginas y espejos de contactos en bobinas.
* **☁️ Nube y Exportación:**
  * Guardado local en formato `.json` o sincronización y compartición en la nube mediante Firebase.
  * Exportación a imagen (PNG / SVG) y listado de materiales (BOM).

### Uso y Atajos de teclado

| Acción | Atajo |
| :--- | :--- |
| **Buscar componentes** | `Ctrl + K` |
| **Dibujar cable / Seleccionar** | `W` / `Esc` |
| **Rotar / Voltear componente** | `R` / `F` |
| **Iniciar / Detener simulación** | `F5` o `Espacio` |
| **Deshacer / Rehacer** | `Ctrl + Z` / `Ctrl + Y` |
| **Copiar / Pegar** | `Ctrl + C` / `Ctrl + V` |
| **Mover lienzo / Zoom** | `Botón central` / `Rueda del ratón` |

### Instalación y Ejecución

La aplicación está desarrollada bajo una **arquitectura de archivo único** (HTML/CSS/JS puro, sin dependencias externas de compilación):

1. Descarga o clona este repositorio:
   ```bash
   git clone https://github.com/usuario/kableo.git
   ```
2. Abre el archivo `index.html` en cualquier navegador web moderno (Chrome, Firefox, Edge, Safari).
3. *(Opcional)* Para habilitar el guardado en la nube, configura las credenciales de tu proyecto Firebase en el código.
