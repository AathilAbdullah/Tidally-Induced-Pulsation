# Research Methodology to Validate Tidal Influence of Exoplanets on Stellar Pulsations

This methodology is designed to validate the tidal influence of exoplanets on host star pulsations using only **observational data** (e.g., TESS light curves) without relying on theoretical stellar models like MESA or GYRE.

---

### **1. Research Objectives**
- Detect and analyze pulsation frequencies in the light curves of stars hosting exoplanets.
- Validate the influence of tidal forces by identifying correlations between pulsation frequencies and the orbital properties of the planet.

---

### **2. Target Star Selection**
1. **Criteria for Star Selection**:
   - Select stars with known **transiting exoplanets** from the TESS TOI Catalog or Exoplanet Archive.
   - Focus on stars that are likely pulsators, such as δ Scuti, γ Dor, or other variable stars that are known to exhibit pulsations.
   - Choose stars with exoplanet orbital periods between **0.5–10 days**, ensuring measurable tidal interactions.

2. **Source of Data**:
   - Utilize **TESS light curves** for selected stars. For best results, use **TASOC CBV-corrected data** to reduce noise and enhance the quality of the light curve analysis.

3. **Number of Stars**:
   - The initial study will focus on **10 target stars** with well-characterized planetary and stellar parameters to ensure the analysis is manageable yet comprehensive.

---

### **3. Data Collection**
1. **Download Light Curves**:
   - Retrieve light curves from the TESS mission. Ensure that the light curves are pre-processed to remove outliers, normalize the flux data, and handle any missing values.
   
2. **Collect Exoplanet Parameters**:
   - Obtain exoplanet orbital parameters such as **orbital period**, **eccentricity**, and **semi-major axis** from reliable sources like NASA’s Exoplanet Archive or TESS TOI Catalog.

---

### **4. Data Analysis**
#### **4.1 Frequency Extraction**
- Extract pulsation frequencies from the light curves using the **Pyriod** Python package, which allows for efficient period analysis.
- This step involves using the Lomb-Scargle periodogram or other similar methods to identify significant periodic signals in the light curves, which may correspond to stellar pulsations.
- The resulting **Power vs. Frequency** plot helps locate significant peaks that indicate potential pulsation modes of the star.

#### **4.2 Orbital Frequency Matching**
- Compute the **orbital frequency** of the exoplanet from its **orbital period (T_orbit)** using the formula:
  \[
  f_{\text{orbit}} = \frac{1}{T_{\text{orbit}}}
  \]
- Compare the pulsation frequencies to check if they match **integer harmonics** of the orbital frequency, i.e., if:
  \[
  f_{\text{pulsation}} = n \cdot f_{\text{orbit}} \quad \text{where } n \in \{1, 2, 3, \dots\}
  \]
- Flag matches within a tolerance range (e.g., \( \Delta f = \pm 0.01 \)) as potential tidal pulsations.

#### **4.3 Phase Coherence Analysis**
- Investigate if the phase of pulsation frequencies, which match the orbital frequency or its harmonics, remains consistent over time.
- Consistent phase behavior suggests a tidal origin for the pulsations, as opposed to intrinsic stellar pulsations, which may vary significantly over time.

#### **4.4 Amplitude Correlation**
- Measure the amplitude of significant pulsation frequencies and compare them to detect any outliers.
- Tidal pulsation modes, driven by the exoplanet’s gravitational influence, often exhibit larger amplitudes compared to intrinsic stellar pulsations.
- Identify pulsations near the orbital frequency or its harmonics that have higher amplitudes, which could indicate tidal interactions.

#### **4.5 Comparative Analysis**
- Conduct a comparative analysis across the 10 target stars to identify any trends.
  - For instance, do stars with more massive, close-in planets exhibit stronger tidal modes?
  - Are stars with similar stellar characteristics (e.g., mass, temperature, etc.) and planetary parameters (e.g., orbital period, eccentricity) showing consistent tidal pulsation patterns?

---

### **5. Validation Criteria**
To validate the presence of tidal influence on stellar pulsations, the following criteria are used:
1. **Frequency Match**: The pulsation frequencies must closely match the orbital frequency or its harmonics.
2. **Amplitude Outliers**: Frequencies near the orbital frequency or its harmonics should exhibit larger amplitudes compared to other stellar pulsations.
3. **Phase Stability**: Pulsation modes matching the orbital frequency or its harmonics should display stable phases over time.
4. **Consistency Across Systems**: Stars with similar stellar and planetary characteristics should exhibit similar tidal pulsation signatures, strengthening the hypothesis of tidal interactions.

---

### **6. Expected Outputs**
1. **Tables**:
   - A table of significant pulsation frequencies for each star, including their amplitudes and whether they match the orbital frequency or its harmonics.
   - A table of the orbital and stellar parameters for each system, such as the orbital period, eccentricity, and stellar mass, which can provide context for the tidal interaction.

2. **Plots**:
   - **Light Curves**: Preprocessed light curves for each star, showing the raw data after outlier removal and normalization.
   - **Periodograms**: Power vs. Frequency plots for each star, showing the pulsation frequencies identified through the period analysis.
   - **Amplitude vs. Frequency**: A plot showing the amplitude of each pulsation frequency to identify any outliers associated with the orbital frequency or its harmonics.

3. **Statistical Summary**:
   - A summary of the percentage of systems that show evidence of tidal pulsations.
   - Statistical analysis of trends based on planetary mass, orbital period, eccentricity, or other relevant parameters.

---

### **7. Challenges**
1. **Noise in Light Curves**: Instrumental noise or stellar activity may obscure the tidal signal, making it challenging to detect.
2. **Sample Size**: With only 10 stars in the initial study, the sample size may be too small to draw robust general conclusions, though it will provide initial insights.
3. **Ambiguity**: Some pulsation frequencies may overlap with other stellar oscillation modes, making it difficult to conclusively identify tidal pulsations without further analysis.

---

### **8. Conclusion**
This methodology aims to directly validate the tidal influence of exoplanets on stellar pulsations using observational data from the TESS mission. By focusing on harmonic matching, amplitude, and phase stability, this approach complements theoretical studies and provides robust evidence for tidally excited pulsations. This approach is an essential step toward understanding the interaction between exoplanets and their host stars, without relying on theoretical models, by focusing entirely on observational data and its analysis.

---

