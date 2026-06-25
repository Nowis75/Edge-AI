# AI na hraně

Doprovodný repozitář ke knize **AI na hraně – Implementace Edge AI do embedded systémů prakticky**.

Tento repozitář obsahuje praktické notebooky, ukázkové datové soubory, exportované modely a experimenty pro vývoj Edge AI aplikací. Navazuje na knihu Milana Nováka vydanou Nakladatelstvím Jihočeské univerzity v Českých Budějovicích v roce 2026 a slouží jako pracovní základ pro studium i vlastní experimenty s nasazováním strojového učení do embedded zařízení.

![Language](https://img.shields.io/badge/language-Python%20%7C%20Jupyter-blue)
![Edge AI](https://img.shields.io/badge/topic-Edge%20AI-orange)
![TinyML](https://img.shields.io/badge/topic-TinyML-green)
![TensorFlow Lite](https://img.shields.io/badge/framework-TensorFlow%20Lite-ff6f00)
![Platform](https://img.shields.io/badge/platform-ESP32--S3%20%7C%20Raspberry%20Pi-lightgrey)

## O projektu

Edge AI označuje nasazení algoritmů umělé inteligence přímo na koncová zařízení v blízkosti zdroje dat. Místo nepřetržitého odesílání surových dat do cloudu probíhá inference lokálně – na mikrokontroléru, jednodeskovém počítači, chytré kameře, senzorickém uzlu nebo jiné embedded platformě.

Cílem tohoto repozitáře je ukázat celý praktický řetězec vývoje Edge AI řešení:

- sběr a příprava dat,
- explorace a předzpracování,
- extrakce příznaků,
- návrh a trénování modelu,
- validace a testování,
- optimalizace a kvantizace,
- export do formátu TensorFlow Lite,
- nasazení na embedded zařízení,
- práce s obrazem, zvukem a senzorickými daty,
- integrace s platformami jako TensorFlow Lite Micro a Edge Impulse.

Repozitář je koncipován jako praktická vrstva ke knize. Kniha poskytuje širší kontext, teoretické vysvětlení, architektury, rozhodovací kritéria a implementační postupy. Tento repozitář poskytuje spustitelné ukázky, modely a datové podklady.

## Pro koho je repozitář určen

Materiály jsou určeny především pro:

- vývojáře embedded systémů,
- IoT vývojáře,
- technické studenty,
- inženýry pracující s mikrokontroléry,
- vývojáře, kteří chtějí převádět ML modely z Pythonu do zařízení,
- autory prototypů s ESP32-S3, Raspberry Pi nebo podobným hardwarem,
- čtenáře knihy **AI na hraně**.

Předpokládá se základní znalost programování v Pythonu. Pro embedded část je vhodná alespoň orientační znalost C/C++, mikrokontrolérů, práce se senzory a vývojového prostředí pro ESP32 nebo Raspberry Pi.

## Návaznost na knihu

Kniha **AI na hraně – Implementace Edge AI do embedded systémů prakticky** postupuje od základních principů strojového učení až po konkrétní implementace na reálných zařízeních. Věnuje se zejména následujícím oblastem:

1. Úvod do Edge AI, Edge ML a TinyML.
2. Architektura Edge computingu a vztah mezi cloudem, near edge a far edge.
3. Životní cyklus Edge AI projektu.
4. Základy strojového učení a metriky hodnocení modelů.
5. Neuronové sítě v embedded systémech.
6. TensorFlow Lite pro mikrokontroléry.
7. Edge Impulse jako vývojová platforma.
8. MLOps pro Edge AI.
9. Vývojový workflow TensorFlow Lite pro MCU.
10. Detekce objektů pomocí FOMO.
11. Nasazení modelu na ESP32-S3.
12. Optimalizace vizualizace detekcí, WebSocket komunikace, MJPEG stream a webové GUI.

Repozitář z těchto témat vybírá praktické části a poskytuje soubory, které lze spustit, upravovat a použít jako základ vlastního projektu.

## Hlavní témata

### Edge AI

Lokální inference na zařízení, nízká latence, provoz bez trvalého připojení k internetu, ochrana soukromí a omezení přenosu dat.

### TinyML

Nasazení malých modelů na zařízení s omezenou RAM, flash pamětí, výkonem a energetickým rozpočtem. Typicky mikrokontroléry, chytré senzory a bateriově napájené uzly.

### TensorFlow Lite a TensorFlow Lite Micro

Převod modelů z TensorFlow/Keras do `.tflite`, kvantizace, optimalizace a příprava modelu pro nasazení na embedded platformy.

### Edge Impulse

Alternativní vývojová pipeline pro sběr dat, návrh impulsu, trénování, validaci a deployment modelů na edge zařízení.

### Detekce objektů

Praktické použití lehkých modelů pro detekci objektů, včetně přístupu FOMO vhodného pro omezený hardware.

### Audio a senzorická data

Ukázky práce se zvukem, MFCC příznaky, klasifikací audia a jednoduchými senzorickými daty.

## Struktura repozitáře

```text
Edge-AI/
├── TFlite/
│   ├── Dataset/
│   └── Model/
├── 2.2.5_FeatureExtraction.ipynb
├── 2.5.5_FeatureExtracion_01.ipynb
├── 2.5.6_ModelTrain.ipynb
├── 2.5.7_ValidationTesting.ipynb
├── 2.5.8_Optimalization.ipynb
├── 2.5.9_Deployment.ipynb
├── 3.0_typeOfML.ipynb
├── 3.4.1_Metrics.ipynb
├── 3.4.2_MetricsRegres.ipynb
├── 3.4.3_MetricForDetectObj.ipynb
├── 3.5.0_TypickeUlohyML.ipynb
├── 4.2.0_perceptron.ipynb
├── 4.3.0_ActivationF.ipynb
├── 4.4.0_cnn.ipynb
├── 7.0.0_TFLiteWorkflow.ipynb
├── 7.1.0_SnapPhoto.ipynb
├── 8.4.3_SnapPhotoAndSendToEdgeImpulse.ipynb
├── *.tflite
├── *.wav
├── *.csv
├── *.json
├── *.png
└── README.md
```

## Doporučená studijní cesta

Pro systematické studium je vhodné postupovat v tomto pořadí:

| Krok | Oblast | Doporučené soubory |
|---:|---|---|
| 1 | Základní orientace v ML | `3.0_typeOfML.ipynb`, `3.5.0_TypickeUlohyML.ipynb` |
| 2 | Příznaky a příprava dat | `2.2.5_FeatureExtraction.ipynb`, `2.5.5_FeatureExtracion_01.ipynb` |
| 3 | Trénování modelu | `2.5.6_ModelTrain.ipynb` |
| 4 | Validace a testování | `2.5.7_ValidationTesting.ipynb` |
| 5 | Metriky | `3.4.1_Metrics.ipynb`, `3.4.2_MetricsRegres.ipynb`, `3.4.3_MetricForDetectObj.ipynb` |
| 6 | Neuronové sítě | `4.2.0_perceptron.ipynb`, `4.3.0_ActivationF.ipynb`, `4.4.0_cnn.ipynb` |
| 7 | TensorFlow Lite workflow | `7.0.0_TFLiteWorkflow.ipynb` |
| 8 | Optimalizace a deployment | `2.5.8_Optimalization.ipynb`, `2.5.9_Deployment.ipynb` |
| 9 | Kamera a obrazová data | `7.1.0_SnapPhoto.ipynb` |
| 10 | Edge Impulse integrace | `8.4.3_SnapPhotoAndSendToEdgeImpulse.ipynb` |

## Přehled vybraných notebooků

### `2.2.5_FeatureExtraction.ipynb`

Ukázka extrakce příznaků. Téma odpovídá části knihy věnované přípravě vstupních dat před trénováním modelu. V Edge AI je extrakce příznaků důležitá zejména proto, že vhodně připravený vstup může výrazně zmenšit nároky modelu na výpočetní výkon.

### `2.5.6_ModelTrain.ipynb`

Notebook zaměřený na návrh a trénování modelu. Slouží jako praktický krok mezi přípravou dat a validací modelu.

### `2.5.7_ValidationTesting.ipynb`

Validace a testování modelu. V Edge AI nestačí sledovat pouze přesnost; důležité jsou také robustnost, velikost modelu, rychlost inference a chování na datech mimo trénovací množinu.

### `2.5.8_Optimalization.ipynb`

Optimalizace a zmenšování modelu. Téma zahrnuje postupy, které jsou pro TinyML kritické: kvantizace, snížení paměťové stopy a příprava modelu na zařízení s omezenými prostředky.

### `2.5.9_Deployment.ipynb`

Nasazení modelu na embedded zařízení. Praktický přechod od modelu natrénovaného v Pythonu k modelu připravenému pro lokální inferenci.

### `3.4.*_Metrics*.ipynb`

Notebooky věnované metrikám pro klasifikaci, regresi a detekci objektů. V embedded praxi je výběr metrik podstatný, protože model s vysokou obecnou přesností nemusí být vhodný pro konkrétní provozní scénář.

### `4.2.0_perceptron.ipynb`, `4.3.0_ActivationF.ipynb`, `4.4.0_cnn.ipynb`

Základy neuronových sítí, aktivačních funkcí a konvolučních sítí. Tyto notebooky tvoří most mezi obecnou teorií ML a architekturami používanými v praktických Edge AI úlohách.

### `7.0.0_TFLiteWorkflow.ipynb`

Praktický TensorFlow Lite workflow: příprava datasetu, vytvoření modelu, trénink, testování, kvantizace a export.

### `7.1.0_SnapPhoto.ipynb`

Práce s kamerou a pořízením obrazových dat. Použitelné jako podpůrný krok pro tvorbu datasetu.

### `8.4.3_SnapPhotoAndSendToEdgeImpulse.ipynb`

Ukázka toku dat směrem do Edge Impulse. Vhodné pro scénáře, kde se data pořizují lokálně a následně používají v cloudové pipeline Edge Impulse.

## Obsažené modely a data

Repozitář obsahuje mimo jiné soubory:

| Soubor | Účel |
|---|---|
| `model.tflite` | Ukázkový model ve formátu TensorFlow Lite |
| `model_float32.tflite` | Model v přesnosti float32 |
| `model_float16.tflite` | Model s redukovanou přesností float16 |
| `model_int8.tflite` | Kvantizovaný model int8 |
| `model_quant.tflite` | Kvantizovaná varianta modelu |
| `mlp_model.tflite` | Model vícevrstvé perceptronové sítě |
| `mobilenet_image_model.tflite` | Obrazový model založený na architektuře MobileNet |
| `audio_mfcc_model.tflite` | Audio model pracující s MFCC příznaky |
| `audio_data.wav` | Ukázkový audio soubor |
| `audio_data_augmented.wav` | Augmentovaný audio soubor |
| `audio_yes.wav` | Ukázka pro jednoduchou klasifikaci zvuku |
| `sensor_data.csv` | Ukázková senzorická data |
| `cnn_model_architecture.json` | Popis architektury CNN modelu |
| `model_architecture.png` | Vizualizace architektury modelu |
| `ei-dicedetect-object-detection-model-evaluation-metrics.json` | Metriky vyhodnocení modelu detekce objektů z Edge Impulse |

## Typický workflow Edge AI projektu

```mermaid
flowchart LR
    A[Definice problému] --> B[Sběr dat]
    B --> C[Čištění a příprava dat]
    C --> D[Extrakce příznaků]
    D --> E[Trénování modelu]
    E --> F[Validace a testování]
    F --> G[Optimalizace a kvantizace]
    G --> H[Export do TensorFlow Lite]
    H --> I[Nasazení na embedded zařízení]
    I --> J[Lokální inference]
    J --> K[Monitoring a aktualizace]
```

Tento workflow odpovídá praktickému postupu, který je v knize rozebrán v kapitole o životním cyklu Edge AI projektu. Důležité je, že vývoj nekončí exportem modelu. U reálného zařízení je nutné sledovat také provozní chování, drift dat, aktualizace modelu a omezení konkrétního hardware.

## Podporované typy úloh

Repozitář se dotýká několika základních kategorií úloh:

- klasifikace,
- regrese,
- detekce objektů,
- detekce anomálií,
- klasifikace zvuku,
- jednoduché zpracování obrazu,
- práce se senzorickými daty.

## Hardware zmiňovaný v knize

Kniha se věnuje výběru hardware pro Edge AI a porovnává různé kategorie zařízení:

| Kategorie | Typické použití | Příklady |
|---|---|---|
| MCU | TinyML, nízká spotřeba, bateriové senzory | ESP32-S3, ESP32-S3-EYE, XIAO ESP32S3 Sense |
| MPU | Výkonnější edge zařízení s Linuxem | Raspberry Pi 4, Raspberry Pi 5, Raspberry Pi Zero 2 W |
| NPU / akcelerátor | Rychlá inference neuronových sítí | Hailo, Coral Edge TPU, integrované AI akcelerátory |
| GPU | Náročnější obrazové a video úlohy | NVIDIA Jetson a podobné platformy |

Repozitář se prakticky orientuje hlavně na Python/Jupyter část, modely TensorFlow Lite a přípravu pro nasazení. Embedded integrace je pak navázána na postupy popsané v knize.

## Instalace

### 1. Klonování repozitáře

```bash
git clone https://github.com/Nowis75/Edge-AI.git
cd Edge-AI
```

### 2. Vytvoření virtuálního prostředí

Linux/macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Instalace základních knihoven

```bash
pip install --upgrade pip
pip install jupyter numpy pandas matplotlib scikit-learn tensorflow opencv-python
```

Podle konkrétního notebooku mohou být potřeba další balíčky. Pokud notebook skončí chybou `ModuleNotFoundError`, doinstalujte chybějící knihovnu pomocí `pip install <nazev-balicku>`.

### 4. Spuštění Jupyter Notebooku

```bash
jupyter notebook
```

Nebo JupyterLab:

```bash
pip install jupyterlab
jupyter lab
```

## Doporučená verze prostředí

Doporučená konfigurace:

- Python 3.10 nebo novější,
- Jupyter Notebook nebo JupyterLab,
- NumPy,
- pandas,
- matplotlib,
- scikit-learn,
- TensorFlow,
- OpenCV,
- TensorFlow Lite runtime podle cílové platformy.

Pro embedded deployment je dále vhodné:

- PlatformIO nebo ESP-IDF pro ESP32-S3,
- Arduino IDE tam, kde dává smysl jednodušší workflow,
- Edge Impulse CLI pro práci s Edge Impulse,
- Raspberry Pi OS pro Raspberry Pi scénáře,
- sériový terminál pro ladění cílového zařízení.

## Edge Impulse CLI

Pro práci s Edge Impulse lze použít CLI nástroje. Typická instalace vyžaduje Node.js a npm:

```bash
npm install -g edge-impulse-cli
```

Přihlášení:

```bash
edge-impulse-login
```

Nahrávání dat nebo komunikace se zařízením závisí na konkrétní desce a firmware. Ukázkový postup je rozveden v notebooku `8.4.3_SnapPhotoAndSendToEdgeImpulse.ipynb` a v příslušných kapitolách knihy.

## Práce s TensorFlow Lite modely

Modely `.tflite` v repozitáři slouží k porovnání variant optimalizace a kvantizace.

Typický postup:

1. Natrénovat model v TensorFlow/Keras.
2. Ověřit model na validačních a testovacích datech.
3. Převést model do TensorFlow Lite.
4. Otestovat přesnost převedeného modelu.
5. Provést kvantizaci, typicky float16 nebo int8.
6. Porovnat přesnost, velikost modelu a rychlost inference.
7. Připravit model pro cílové zařízení.

Zjednodušený příklad konverze:

```python
import tensorflow as tf

model = tf.keras.models.load_model("model.keras")
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()

with open("model.tflite", "wb") as f:
    f.write(tflite_model)
```

Příklad kvantizace float16:

```python
import tensorflow as tf

converter = tf.lite.TFLiteConverter.from_keras_model(model)
converter.optimizations = [tf.lite.Optimize.DEFAULT]
converter.target_spec.supported_types = [tf.float16]

model_float16 = converter.convert()

with open("model_float16.tflite", "wb") as f:
    f.write(model_float16)
```

## Praktické poznámky k Edge AI

Při vývoji modelu pro embedded zařízení nestačí sledovat jen přesnost modelu. U reálného Edge AI projektu je nutné sledovat také:

- velikost modelu ve flash paměti,
- velikost pracovních tenzorů v RAM,
- dobu inference,
- spotřebu energie,
- dostupnost instrukčních optimalizací,
- podporu operátorů v TensorFlow Lite Micro,
- kvalitu vstupních dat ze senzorů,
- provozní teplotu zařízení,
- možnost aktualizace modelu v terénu,
- reakci systému při výpadku konektivity.

## Typické scénáře použití

### Detekce objektů na ESP32-S3

Zařízení pořizuje obraz z kamery, provede předzpracování, spustí lehký detekční model a lokálně rozhodne, zda je v obraze hledaný objekt. Výsledek lze zobrazit, uložit nebo odeslat přes Wi-Fi.

### Klasifikace zvuku

Mikrofon pořizuje krátká audio okna, z nichž se vypočítají MFCC příznaky. Ty vstupují do malého modelu, který klasifikuje zvukovou událost, například jednoduché klíčové slovo.

### Detekce anomálií ze senzorů

Senzorická data se průběžně vyhodnocují lokálně. Model může upozornit na odchylku bez nutnosti posílat kompletní datový proud do cloudu.

### Edge Impulse pipeline

Data se pořídí na zařízení, nahrají do Edge Impulse, zde se navrhne impulse, provede trénink a výsledný model se nasadí zpět do embedded zařízení.

## Doporučení pro vlastní experimenty

- Začněte s malým modelem a jednoduchým datasetem.
- Nejprve ověřte funkčnost v Pythonu.
- Teprve poté model převádějte do `.tflite`.
- Po každé optimalizaci znovu měřte přesnost.
- U embedded zařízení vždy měřte reálnou dobu inference.
- Nepředpokládejte, že model funkční v desktopovém Pythonu bude automaticky vhodný pro MCU.
- U obrazových modelů zmenšujte rozlišení vstupu co nejdříve v pipeline.
- U zvukových modelů věnujte pozornost kvalitě vstupního signálu a stabilitě MFCC příznaků.
- U senzorických modelů sledujte drift dat a rozdíl mezi laboratorními a provozními podmínkami.

## Časté problémy

### Notebook nejde spustit kvůli chybějící knihovně

Doinstalujte chybějící balíček:

```bash
pip install <nazev-balicku>
```

### TensorFlow Lite model má výrazně horší přesnost než původní model

Zkontrolujte předzpracování vstupů, typ kvantizace, rozsah reprezentativního datasetu a datové typy vstupních tenzorů.

### Model je příliš velký pro mikrokontrolér

Zmenšete architekturu, snižte rozlišení vstupu, použijte int8 kvantizaci nebo jednodušší typ modelu. U některých úloh může být vhodnější klasický ML model než hluboká neuronová síť.

### Inference je pomalá

Zkontrolujte velikost vstupu, počet parametrů, podporu operátorů, typ kvantizace a možnost využití optimalizovaných knihoven pro cílovou platformu.

### Edge Impulse zařízení se nepřipojuje

Ověřte firmware, sériový port, oprávnění k portu, přihlášení do Edge Impulse CLI a správné mapování pinů kamery nebo senzoru.

## Doporučená struktura vlastního projektu

```text
my-edge-ai-project/
├── data/
│   ├── raw/
│   ├── processed/
│   └── representative/
├── notebooks/
├── models/
│   ├── keras/
│   └── tflite/
├── firmware/
├── docs/
├── tests/
└── README.md
```

Takové rozdělení pomáhá oddělit experimenty, datové sady, modely a firmware pro cílové zařízení.

## Bibliografická poznámka

**AI na hraně – Implementace Edge AI do embedded systémů prakticky**  
Autor: **Milan Novák**  
Vydání: první  
Nakladatelství: Jihočeská univerzita v Českých Budějovicích, 2026  
ISBN PDF: **978-80-7694-167-0**

## Jak citovat

Pokud používáte tento repozitář jako podpůrný materiál ke studiu nebo výuce, uveďte knihu a repozitář:

```text
Novák, Milan. AI na hraně: Implementace Edge AI do embedded systémů prakticky.
České Budějovice: Nakladatelství Jihočeské univerzity v Českých Budějovicích, 2026.
Doprovodné zdrojové kódy: https://github.com/Nowis75/Edge-AI
```

## Stav repozitáře

Repozitář je praktickým doprovodným materiálem ke knize. Některé soubory představují ukázky, mezivýsledky nebo exportované modely určené k demonstraci konkrétního kroku vývoje. Struktura se může dále rozšiřovat podle doplňovaných příkladů.

## Autor

**Milan Novák**

Autor knihy **AI na hraně – Implementace Edge AI do embedded systémů prakticky**.

