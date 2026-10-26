---
layout: page
title: Interior modelling of Steam Worlds
permalink: /research/interior-modelling/
description: Exploring the interiors and thermal evolution of water-rich exoplanets
img: assets/img/Superionic-Ice-Giant_2880x1620.jpg
importance: 1
category: work
related_publications: true
mermaid:
  enabled: true
  zoomable: true
_styles: |
  .interior-illustration {
    position: relative;
    aspect-ratio: 2880 / 1053;
    overflow: hidden;
  }
  .interior-illustration img {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    /* Remove 20% above and 15% below the original image. */
    object-position: 50% 57.142857%;
  }
  .steam-world-video {
    max-width: 560px;
    margin-inline: auto;
  }
---

I uses structure models to connect observable properties of planets (mass, radius, temperature, age, etc.) to their bulk composition. My research focuses on **steam worlds**: water-rich planets whose intense stellar irradiation produces a steam atmosphere above (runaway greenhouse effect), and a deep water envelope in supercritical state (and other exotic phases of water: plasma, superionic, high pressure ices, etc.).

<div class="interior-illustration rounded z-depth-1">
  {% include figure.liquid loading="eager" path="assets/img/Superionic-Ice-Giant_2880x1620.jpg" alt="Artist's exploded view of an ice giant, showing its central core and surrounding layers" %}
</div>
<div class="caption">
  Artist's impression of steam worlds's layered interior, shown in an exploded view. Illustration: <a href="https://www.quantamagazine.org/black-hot-superionic-ice-may-be-natures-most-common-form-of-water-20190508/">@iammoteh for Quanta Magazine</a>.
</div>

## Model development

These models have developed through a series of collaborations, for the immediate purpose of interpreting data from new space missions such as Kepler, Gaia, TESS, JWST and in the near future PLATO and ARIEL. The diagram below traces these developments and the connections between models.

<!-- Edit the quoted labels to change model names and researchers.
     Use the box IDs to edit connections; disable Mermaid lines with %% comments. -->

```mermaid
flowchart LR
    %% Boxes: model name, researcher, year, and main contribution
    Sotin2007["Sotin 2007<br/>Solar System rocky and<br/>water rich planets"]
    Brugger["Brugger+2016,+2017<br/>MSEI model"]
    Mousis2020["Mousis,Deleuil,<u>Aguichine</u>+2020<br/>Steam Worlds"]
    Aguichine2021["<u>Aguichine</u>+2021<br/>IOP model: mass-radius relations<br/>of steam worlds"]
    Aguichine2025["<u>Aguichine</u>+2025<br/>SWE model: thermal evolution<br/>of steam worlds"]
    Kempton2023["Kempton+2023<br/>Atmospheres of steam worlds"]
    Acuna2021["Acuña,incl. <u>Aguichine</u>+2021<br/>Application to TRAPPIST-1"]
    %% Acuna2024["Acuña+2024<br/>H<sub>2</sub>-He planets<br/>no longer steam worlds"]

    %% Connections: direct extensions (solid) and influences (dashed)
    Sotin2007 -.->|"Inspired (physics<br/>and mineralogy)"| Brugger
    Brugger -->|Added thermal gradient<br/>and atmosphere| Mousis2020
    Mousis2020 -->|Coupling with atmosphere<br/>Extended validity range<br/>Fixed numerical instabilities| Aguichine2021
    Aguichine2021 -->|Added thermal evolution| Aguichine2025
    Kempton2023 -->|Coupling with interior| Aguichine2025
    Aguichine2021 -->|Application with<br/>Bayesian analysis| Acuna2021
    %% Acuna2021 -->|Application with<br/>Bayesian analysis| Acuna2024
```
Solid arrows show direct extensions; dashed arrows show influence. Acronyms and references at the bottom of the page.

## Thermal evolution of steam worlds

My **Irradiated Ocean Planets (IOP)** model explored how hot water envelopes and steam atmospheres shape planetary mass–radius relationships {% cite 2021ApJ...914...84A %}. In previous studies, water worlds were often thought as objects with extended oceans of condensed water: liquid or high pressure ice. This model showed that steam worlds have much larger radii, making them great candidates to explain the radii of hundreds of sub-Neptunes found with Kepler.

A planet's radius depends on its thermal history as well as its composition. In the **Steam World Evolution (SWE)** model, my collaborators and I couple an interior model, which stores the planet's energy, to a steam atmosphere model, which controls how quickly that energy escapes. This lets us follow the cooling and contraction of water-rich planets over time {% cite 2025ApJ...988..186A %}. Age dependence is one avenue of breaking the degeneracy between steam worlds and gas dwarfs, using revised age calculations from Gaia, and in the near future PLATO.

The latest extension, **Steam World Evolution Extended in Temperature (SWEET)**, broadens the atmosphere grid to equilibrium temperatures of **400–1500 K**, allowing us to explore a wider range of irradiated planets. The [SWEET evolutionary tracks](https://zenodo.org/records/21403288) are publicly available for comparison with observations and estimates of planetary water content.

<div class="steam-world-video">
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/U0_KSvwwedI" title="Thermal evolution of a steam world" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
</div>
<div class="caption">
  Cooling and contraction of a model steam world. Colors indicate temperature.
</div>

## Models and data

- [IOP mass–radius relations](https://archive.lam.fr/GSP/MSEI/IOPmodel/)
- [SWE evolutionary tracks](https://zenodo.org/records/17811145)
- [SWEET evolutionary tracks](https://zenodo.org/records/21403288)

References: [Aguichine et al. 2025](https://ui.adsabs.harvard.edu/abs/2025ApJ...988..186A), [Kempton et al. 2023](https://ui.adsabs.harvard.edu/abs/2023ApJ...953...57K), [Aguichine et al. 2021](https://ui.adsabs.harvard.edu/abs/2021ApJ...914...84A), [Acuña et al. (incl. Aguichine) 2021](https://ui.adsabs.harvard.edu/abs/2021A&A...647A..53A), [Mousis et al. (incl. Aguichine) 2020](https://ui.adsabs.harvard.edu/abs/2020ApJ...896L..22M), [Brugger et al. 2017](https://ui.adsabs.harvard.edu/abs/2017ApJ...850...93B), [Brugger et al. 2016](https://ui.adsabs.harvard.edu/abs/2016ApJ...831L..16B), [Sotin 2007](https://ui.adsabs.harvard.edu/abs/2007Icar..191..337S)
