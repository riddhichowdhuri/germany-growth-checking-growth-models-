# Germany: Growth & Development — Solow, Ramsey–Cass–Koopmans and OLG

## Project overview

This project studies Germany's long-run economic growth and development using three complementary growth frameworks:

1. **Solow–Swan Growth Model** — focuses on capital accumulation, labour/population growth and technological progress.
2. **Ramsey–Cass–Koopmans (RCK) Model** — introduces forward-looking household optimisation, consumption and saving decisions.
3. **Overlapping Generations (OLG) Model** — focuses on demographic structure, saving, capital accumulation and dynamic efficiency.

The purpose is not to treat one model as universally sufficient, but to compare what each framework can explain about Germany's growth experience and where each framework has limitations.

The project combines theoretical model development with empirical regression, steady-state/transition analysis, graphical analysis and a final model comparison.

---

## Why Germany?

Germany provides a useful case for growth-and-development analysis because its growth experience has involved major structural changes:

- post-war reconstruction and rapid industrial expansion;
- division into West Germany and East Germany;
- the 1973 oil shock and subsequent slowdown;
- reunification in 1990;
- increasing importance of technology and human capital;
- a large manufacturing and export-oriented sector;
- demographic ageing and strong saving behaviour.

The presentation therefore uses Germany to examine how growth theory performs across different stages of development.

---

## Research questions

The project asks:

- How well does the Solow model explain Germany's growth and convergence?
- What role do capital, labour and technology play in Germany's output?
- How can the Ramsey model explain saving, consumption and capital accumulation?
- What does the OLG framework add when demographics and intergenerational saving are considered?
- Does the empirical evidence suggest dynamic efficiency or dynamic inefficiency?
- Which framework provides the most useful explanation of modern Germany?

---

# 1. Solow–Swan Growth Model

### Theoretical framework

The Solow model provides a neoclassical framework for long-run growth. The project uses a Cobb–Douglas production function and examines the interaction between capital accumulation, labour/population growth and technological progress.

The capital accumulation equation used in the presentation is:

\[
\dot{k}=sf(k)-(n+g+\delta)k
\]

where:

- \(s\) = saving rate
- \(n\) = population growth
- \(g\) = technological progress
- \(\delta\) = depreciation
- \(k\) = capital per effective worker

The steady state occurs when:

\[
\dot{k}=0
\]

so actual investment equals break-even investment.

### Empirical analysis

A Barro-style regression was used to examine growth and conditional convergence over two periods:

- **1962–1991:** post-war/reconstruction and pre-reunification period
- **1992–2024:** post-reunification period

The presentation reports **weak empirical support for the basic Solow model**. Although the sign of initial income is consistent with conditional convergence, the relevant coefficients are statistically insignificant.

### Interpretation

The results suggest that Germany's growth cannot be explained by capital accumulation alone. Structural transformation, technology and human capital appear important, particularly in the post-reunification period.

---

# 2. Ramsey–Cass–Koopmans Model

The Ramsey framework extends the growth analysis by allowing households to make forward-looking consumption and saving decisions.

The project considers the dynamic equations:

\[
\dot{k}=f(k)-c-(n+g+\delta)k
\]

and

\[
\frac{\dot{c}}{c}=\frac{1}{\theta}[f'(k)-\rho-\delta]
\]

where consumption and capital jointly determine the economy's transition toward steady state.

### Production-function estimation

A Cobb–Douglas production function was estimated using OLS in Gretl:

\[
\ln Y=\beta_0+\alpha\ln K+\beta\ln L
\]

The presentation reports:

- labour has a **strong and statistically significant** effect on output;
- capital accumulation has a positive but relatively smaller estimated effect;
- \(R^2 \approx 0.938\), indicating high explanatory power for the estimated production relationship.

### Euler equation / consumption behaviour

The project also estimates a log-linearised Euler equation using GMM:

\[
\Delta\ln C_t=\alpha+\beta r_{t-1}+\epsilon_t
\]

The reported coefficient on the lagged real interest rate is approximately:

\[
\beta=0.037
\]

and is statistically significant.

The project interprets this small coefficient as evidence of a relatively weak consumption response to changes in the real interest rate and therefore low intertemporal substitution.

### Limitation

The presentation explicitly notes that the Ramsey phase diagram is sensitive to parameter assumptions and limited data. Therefore, the graphical steady-state analysis should be interpreted as an illustrative model exercise rather than a definitive estimate of Germany's structural equilibrium.

---

# 3. Overlapping Generations (OLG) Model

The OLG framework introduces an explicit intergenerational dimension.

Individuals are represented as:

- **young:** earn labour income, consume and save;
- **old:** consume from accumulated savings.

Young people's saving becomes capital available in the next period.

### Variables

The project uses macroeconomic variables including:

- population growth \(n\)
- GDP growth \(g\)
- CPI / inflation \(\pi\)
- nominal interest rate \(i\)
- real interest rate \(r\)
- gross saving
- capital transition

The real interest rate is calculated using the Fisher-style relationship:

\[
r=i-\pi
\]

The project considers the combined growth rate:

\[
n+g
\]

### Dynamic efficiency

The key comparison is:

\[
r^* \quad \text{vs.} \quad n+g
\]

Dynamic inefficiency is defined in the project as:

\[
r^*<n+g
\]

and dynamic efficiency as:

\[
r^*>n+g
\]

A dummy variable is used to classify the periods accordingly.

### Interpretation

The presentation highlights:

- ageing population effects;
- strong saving behaviour;
- periods in which \(r<n+g\);
- possible dynamic inefficiency;
- changes in saving and capital accumulation over time.

---

# 4. Data

The accompanying Excel workbook contains annual observations and constructed variables used in the project.

The workbook contains **65 annual observations from 1959–2023** and includes variables such as:

- real GDP
- capital stock
- population
- human capital index
- saving rate
- real interest rate
- depreciation rate
- labour force
- consumption share
- total factor productivity
- consumption
- labour share of output
- output per worker
- capital per worker
- population growth
- GDP growth
- technological growth
- capital share
- estimated productivity
- actual investment
- break-even investment
- change in capital
- consumption
- consumption growth
- estimated preference parameter
- RCK capital accumulation
- consumption/capital steady-state condition

See [`data/Germany_Growth_Development_Data.xlsx`](data/Germany_Growth_Development_Data.xlsx) for the workbook and [`data/Germany_Growth_Development_Data.csv`](data/Germany_Growth_Development_Data.csv) for a flat-data version.

> **Data-period note:** Different empirical exercises in the presentation use different periods. The Solow convergence regressions use 1962–1991 and 1992–2024; the Ramsey production-function exercise uses 1991–2023; the OLG discussion uses 1976–2024. The supplied Excel workbook itself contains annual observations from 1959–2023. These periods should not be treated as interchangeable.

---

# 5. Figures

The `figures/` folder contains the supplied empirical and model-dynamics figures, including:

- Solow actual investment vs. break-even investment
- capital accumulation
- Solow phase diagrams
- change in capital per worker
- RCK capital accumulation
- RCK steady-state / consumption-capital diagrams
- output per worker and steady-state comparisons
- Barro regression outputs

The figures are kept as individual image files so they can be viewed and referenced separately on GitHub.

---

# 6. Main findings

### Solow

The evidence provides **weak empirical support** for the basic Solow explanation of Germany's growth.

- Conditional convergence is suggested by the coefficient sign.
- The convergence coefficients are statistically insignificant.
- Investment is not strongly significant in the reported regressions.
- Structural and technological factors appear important.

### Ramsey

The Ramsey framework provides a stronger behavioural interpretation.

- Labour is strongly associated with output.
- The production-function regression has high explanatory power (\(R^2\approx0.938\)).
- Consumption responds positively but weakly to the lagged real interest rate.
- The reported GMM coefficient of approximately 0.037 is interpreted as low intertemporal substitution.
- Forward-looking saving and consumption behaviour provide useful additional information beyond the Solow framework.

### OLG

The OLG model adds the demographic and intergenerational channel.

- Germany's ageing population matters for saving and capital accumulation.
- Saving behaviour is important for the growth process.
- The project identifies periods of \(r<n+g\), interpreted as dynamic inefficiency.
- Saving rises during periods of uncertainty, including the financial crisis and the 2020 period.

### Overall conclusion

The project concludes that Germany's growth is better understood through a combination of **Ramsey and OLG mechanisms** than through capital accumulation alone.

The presentation characterises Germany's development as a shift from:

**capital-driven post-war growth → human-capital-, technology- and institution-supported growth.**

---

# 7. Policy implications

The project derives five broad policy areas:

### Productivity and growth
- invest in human capital and skills;
- strengthen vocational training;
- support technology adoption in SMEs.

### Savings and financial stability
- encourage productive investment channels;
- strengthen financial-market stability;
- promote innovation financing.

### Demographic policy
- pension-system reforms;
- skilled immigration;
- higher female labour-force participation;
- family welfare support.

### Macroeconomic stability
- maintain stable inflation;
- predictable monetary policy;
- reduce economic uncertainty.

### Structural growth
- innovation-driven growth;
- higher labour productivity;
- demographic sustainability;
- long-term competitiveness.

---

# 8. Model comparison

| Model | Main mechanism | What it explains well | Main limitation |
|---|---|---|---|
| **Solow** | Capital, labour & technology | Long-run growth and convergence framework | Limited behavioural/demographic detail |
| **Ramsey** | Optimal saving & consumption | Forward-looking behaviour and transition dynamics | Sensitive to parameters; empirical behavioural channel is relatively weak |
| **OLG** | Demographics & intergenerational saving | Ageing, saving and dynamic efficiency | Stylised two-period structure and sensitivity to measurement |

The project therefore treats the three models as **complementary rather than mutually exclusive**.

---

# 9. Repository structure

```text
germany-growth-development/
│
├── README.md
├── FINDINGS.md
│
├── data/
│   ├── Germany_Growth_Development_Data.xlsx
│   └── Germany_Growth_Development_Data.csv
│
├── figures/
│   ├── solow_barro_regression_1962_1991.jpg
│   ├── solow_barro_regression_1992_2024.jpg
│   ├── solow_actual_vs_break_even_investment.jpg
│   ├── solow_capital_accumulation_over_time.jpg
│   ├── empirical_solow_phase_diagram.jpg
│   ├── rck_capital_accumulation_dot_k.jpg
│   ├── empirical_phase_diagram_growth_path.jpg
│   ├── solow_change_in_capital_per_worker.jpg
│   ├── solow_capital_per_worker_over_time.jpg
│   ├── empirical_phase_diagram_consumption_path.jpg
│   ├── rck_steady_state_consumption_capital.jpg
│   └── output_per_worker_vs_steady_state.jpg
│
├── presentation/
│   └── Germany_Growth_Development_Presentation.pdf
│
└── docs/
    └── SOURCE_NOTES.md
```

---

# 10. Limitations and reproducibility

This repository contains the project presentation, supplied workbook and supplied figures.

The original Python/R/Gretl source scripts used to generate every empirical result were **not included in the materials supplied for this repository build**. Therefore, this repository does not claim full computational reproducibility of the Gretl/GMM/OLS and graphical outputs.

For a fully reproducible research repository, the original:

- Gretl scripts/session files,
- R scripts,
- Python notebooks/scripts,
- raw downloaded datasets,
- and exact data-source links

should be added.

---

## Project materials

- **Presentation:** `presentation/Germany_Growth_Development_Presentation.pdf`
- **Data workbook:** `data/Germany_Growth_Development_Data.xlsx`
- **CSV:** `data/Germany_Growth_Development_Data.csv`
- **Figures:** `figures/`

---

## Academic context

**Course:** Growth & Development  
**Country:** Germany  
**Programme:** FYMSc Economics, Batch 2025–2027  
**Group:** B2

This repository is intended as a portfolio and academic documentation of the group's Germany growth-and-development analysis.
