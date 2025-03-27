# Vorlesung – Mehrkörperprobleme in der Physik

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TobiBu/Nbody-lecture/blob/master/nbody_lecture_colab.ipynb)

Dieses Repository enthält eine interaktive Jupyter Notebook-Vortrag, der sich mit verschiedenen Aspekten von Mehrkörperproblemen in der Physik beschäftigt. Das Notebook kombiniert theoretische Erklärungen, numerische Simulationen und Animationen, um fundamentale Konzepte wie Gravitation, Chaos, Instabilitäten und numerische Integrationsmethoden (z. B. Leapfrog-Integrator) anschaulich darzustellen.

## Inhalte des Notebooks

- **Theoretische Grundlagen:**
  Erklärungen zu Gravitation, dem N-Körper-Problem, Liouvilles Theorem, und der collisionless Boltzmann Equation.

- **Numerische Methoden:**
  - Direkte Kraftberechnung (O(N²))
  - Hierarchische Methoden (Barnes-Hut, Fast Multipole)
  - Particle-Mesh- und Hybrid-Methoden
  - Symplektische Integratoren (Leapfrog)

- **Simulationen und Animationen:**
  - N-Body-Simulationen (z. B. Plummer-Sphäre mit JAX)
  - Simulation gekoppelter Pendel
  - Planetenbahnen im Sonnensystem
  - Vergleich von stabilen Kepler-Orbits und chaotischen Bahnen (2- vs. 3-Körper-Probleme)

- **Interaktive Elemente:**
  Ein Slider zur dynamischen Anpassung der Teilchenanzahl.

## Dateistruktur

- **lehrprobe.ipynb:**
  Das zentrale Jupyter Notebook, das alle Inhalte und Simulationen enthält.

- **README.md:**
  Diese Datei mit einer Zusammenfassung und Anleitung zur Einrichtung.

## Ausführen des Notebooks

### Auf Google Colab

1. Öffne [Google Colab](https://colab.research.google.com/).
2. Wähle im Menü "Datei" → "Notebook öffnen" → "GitHub".
3. Gib die URL dieses GitHub-Repositories ein und wähle das Notebook `lehrprobe.ipynb` aus.
4. Das Notebook wird in Google Colab geladen und kann dort ausgeführt werden (eventuell musst du einige Pakete per `!pip install` nachinstallieren).

**Hinweis** Die Animationen starten nicht automatisch auf Colab, zum Abspielen bitte den Play Button unter den Plots benutzen. Außerdem brauchen die Berechnungen auf Colab wesentlich länger als local auf einem PC.

### Lokales Ausführen mit Conda

1. **Erstelle ein neues Conda-Environment mit allen dependencies:**

   ```bash
   conda env create -f nbody.yml
   ```

2. **Aktiviere das Environment:**

   ```bash
   conda activate nbody
   ```

3. **Starte Jupyter Notebook:**

   ```bash
   jupyter notebook
   ```

3. **Öffne das Notebook `lehrprobe.ipynb` im Browser und führe die Zellen aus.**

### Falls du lieber mit pip arbeitest:

Du kannst auch gerne pip verwenden, dann musst du aber selber die benötigten Pakete installieren und deren dependencies klären.
Keine Garantien meinerseits.

1. **Erstelle ein Conda-Environment:**
     ```bash
     conda create --name nbody python=3.12
     ```

2. **Aktiviere das Environment:**
     ```bash
     conda activate nbody
     ```

3. **Installiere die benötigten Pakete:**

   ```bash
   pip install jax jaxlib numpy matplotlib scipy
   pip install jupyter ipywidgets
   ```

4. **Starte Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
5. **Öffne dieses Notebook und führe die Zellen aus.**

6. **Falls es fehlende Pakete geben sollte - nachinstallieren...**

## Hinweise

- **Rechenintensive Simulationen:**
  Einige Simulationen (insbesondere die N-Body-Simulationen) können bei größeren Teilchenzahlen längere Rechenzeiten in Anspruch nehmen.
- **Interaktive Visualisierungen:**
  Das Notebook enthält interaktive Elemente (z. B. Slider), die in Jupyter Notebook (oder Google Colab) vollständig unterstützt werden.
- **Abhängigkeiten:**
  Achte darauf, das korrekte Conda-Environment zu aktivieren, um Konflikte zwischen verschiedenen Paketversionen zu vermeiden.
