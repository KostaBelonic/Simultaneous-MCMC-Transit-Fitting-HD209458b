# Simultaneous-MCMC-Transit-Fitting-HD209458b
Simultaneous and individual MCMC fitting of multi-wavelength transit light curves of the exoplanet HD 209458b using the batman model.
# Multi-wavelength Transit Modeling of HD 209458b

This repository contains a detailed analysis of the exoplanet HD 209458b
using transit photometry observed in multiple wavelength filters.
The system parameters are determined using Markov Chain Monte Carlo (MCMC)
methods and a physical transit model implemented with the `batman` package.

## Methodology

Two fitting approaches are implemented and compared:

### 1. Individual Fitting
Each photometric filter is fitted independently.
All model parameters (orbital and atmospheric) are allowed to vary separately
for each wavelength.

### 2. Simultaneous Fitting
All light curves are fitted simultaneously.
- Orbital parameters (semi-major axis and inclination) are shared across all filters.
- Planetary radius and limb-darkening coefficients are allowed to vary with wavelength.

This approach reflects the physical expectation that orbital geometry is wavelength-independent,
while stellar atmosphere effects are not.

## Modeling and Inference

- Transit light curves are generated using the `batman` package.
- Parameter estimation is performed using the `emcee` MCMC sampler.
- Posterior distributions are analyzed using corner plots.
- Results are compared with literature values from Knutson et al. (2007).

## Data

The photometric data used in this project were taken from:
Knutson et al. (2007), *The Astrophysical Journal*, 655, 564–575.\
Data were obtained from the NASA Exoplanet Archive (Caltech/IPAC):  
https://exoplanetarchive.ipac.caltech.edu/overview/HD%20209458

## Results

- Orbital parameters obtained from both fitting methods agree within ~1%.
- The planet radius shows wavelength-dependent variations of up to ~3%.
- No statistically significant difference is found between individual and simultaneous fitting.

## Dependencies

See `requirements.txt`.

## Author

Kosta Belonić  
High School of Kladovo  
Mentors:  
- Vesna Milošević (Faculty of Mathematics, University of Belgrade)  
- Filip Mitić (Faculty of Mathematics, University of Belgrade)  
- Dušan Vukadinović (Max Planck Institute for Solar System Research)

## License

This project is intended for academic and educational use.
