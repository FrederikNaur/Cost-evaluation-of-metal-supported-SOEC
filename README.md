This repository contains the cost model used in:

> F. S. Naur, A. Hagen, H. L. Frandsen, A. Nemati, *Bottom-up cost model for metal-supported solid oxide electrolysis cells and stacks* (submitted, 2026).

The model estimates the direct manufacturing cost of planar solid oxide electrolysis (SOE) stacks at high production volume, per single repeating unit (SRU), per kW and per kW and year of operation. It extends the manufacturing framework of Harboe et al. (2020) with step-specific scaling of machine and energy costs, so that changes in cell and stack design propagate to the manufacturing cost.

## Contents

| File | Description |
|---|---|
| `Cost model - Metal support.xlsx` | Metal-supported cell (MSC), tape-cast steel-powder support |
| `Cost model - FE support.xlsx` | Fuel-electrode-supported cell (FESC) |
| `Cost model - Electrolyte support.xlsx` | Electrolyte-supported cell (ESC) |
| `Harboe validation.xlsx` | Recalculation of the light-weight stack of Harboe et al. (2020) |

Each workbook contains the following sheets:

- **Manufacturing results**: cost per SRU and per cm² of active area, split into cell, frame, miscellaneous materials, machining, labour and energy.
- **Performance**: operating point (current density, voltage, temperature) and the conversion to cost per kW.
- **Cross-layer**: cell and stack geometry, steel type, scrap credit and cell discard rate.
- **Cell, Frame, Misc**: material quantities and costs per layer.
- **Manufacturing inputs, Manufacturing calc**: production volume, labour cost, electricity price, and the CAPEX, cycle time, manning, power and scaling rule of each process step.
- **Materials**: material prices and densities.

## Use

Change the inputs in **Cross-layer**, **Cell**, **Materials** and **Performance**; the results update in **Manufacturing results** and **Performance**. The workbooks use `XLOOKUP` and therefore require Excel 2021 / Microsoft 365 or newer.

## Baseline results

| Design | Cost [€/SRU] | Current density [A/cm²] | Cost [€/kW] |
|---|---|---|---|
| MSC | 6.22 | 0.5 | 121 |
| FESC | 6.08 | 1.0 | 59 |
| ESC | 9.26 | 0.8 | 112 |

Prices are in 2018 € (Harboe et al. 2020), not inflation-adjusted.

## Sources

Manufacturing inputs and most material prices are taken from:
S. Harboe et al., *Manufacturing cost model for planar 5 kWel SOFC stacks at Forschungszentrum Jülich*, Int. J. Hydrogen Energy 45 (2020) 8015–8030, https://doi.org/10.1016/j.ijhydene.2020.01.082.
Corrections to their supplementary data are described in the Supplementary Material of the paper.

## Citation

If you use this model, please cite the paper above.
