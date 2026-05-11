# Gradientní boosting rozhodovacích stromů - Gradient Boosting of Decision Trees

Tento repozitář obsahuje kód pro mou bakalářskou práci. Pro správu knihoven se používá nástroj [uv](https://github.com/astral-sh/uv).

Veškeré výpočty probíhaly na zařízení MacBook Air s čipem M2 s 8 grafickými jádry a 16 GB jednotné paměti. Část ladění hyperparametrů probíhala i na zařízení MacBook Air s čipem M1 se 7 grafickými jádry a 8 GB jednotné paměti.

Velká část kódu v práci vyžaduje více výpočetního času, až v řádu hodin.

## Jak projekt zprovoznit (pro Visual Studio Code)

1. **Nainstalujte si nástroj `uv` (pokud jej ještě nemáte nainstalovaný)**
   - Viz [oficiální návod](https://docs.astral.sh/uv/getting-started/installation/).

2. **V terminálu přejděte do základní složky `bachelor_thesis`**
   - Například pomocí `cd` nebo otevřením terminálu ve Visual Studio Code v otevřeném repozitáři.

3. **Nainstalujte závislosti a vytvořte prostředí**
   - Tento příkaz automaticky vytvoří složku `.venv` a nainstaluje verze balíčků, které zaručují funkčnost kódu (podle `uv.lock`).

   ```bash
   uv sync --frozen
   ```

4. **Spuštění ve Visual Studio Code**
   - Otevřete libovolný `.ipynb` soubor.
   - Vpravo nahoře klikněte na **Select Kernel** → **Python Environments** a vyberte prostředí ze složky `.venv`.


## Struktura repozitáře

```text
bachelor_thesis/
├── data/                                      # 🔴 [R] Datové sady (původní jen v rozšířené verzi, zpracované i v základní)
├── eda/                                       # 🔴 [R] Výstupy z exploratorní analýzy
├── hyperparameter_tuning/                     # 🔴 [R] Uložené průběhy ladění hyperparametrů
├── test_results/                              # 🔴 [R] Výsledky testování v metrikách i soubory predikcí
│
├── 01_data_preparation_and_cleaning.ipynb     # 🔴 [R] Čištění dat a příprava pro modelování
├── 02_eda_feature_engineering.ipynb           # 🟢 [Z] Exploratorní analýza a tvorba nových příznaků
├── 03_catboost_hyperparameter_tuning.ipynb    # 🟢 [Z] Ladění parametrů pro model CatBoost
├── 03_gbm_hyperparameter_tuning.ipynb         # 🟢 [Z] Ladění parametrů pro model GBM
├── 03_histgbm_hyperparameter_tuning.ipynb     # 🟢 [Z] Ladění parametrů pro model HistGBM
├── 03_lightgbm_hyperparameter_tuning.ipynb    # 🟢 [Z] Ladění parametrů pro model LightGBM
├── 03_ngboost_hyperparameter_tuning.ipynb     # 🟢 [Z] Ladění parametrů pro model NGBoost
├── 03_pgbm_hyperparameter_tuning.ipynb        # 🟢 [Z] Ladění parametrů pro model PGBM
├── 03_tabpfn_testing.ipynb                    # 🟢 [Z] Testování modelu TabPFN
├── 03_xgboost_hyperparameter_tuning.ipynb     # 🟢 [Z] Ladění parametrů pro model XGBoost
├── 04_model_train_test_results.ipynb          # 🟢 [Z] Finální trénování a vyhodnocení na testovací sadě
├── 05_results_comparison.ipynb                # 🔴 [R] Porovnání výkonnosti všech testovaných modelů
├── 06_ensemble_of_ensembles.ipynb             # 🔴 [R] Tvorba a vyhodnocení ansámblových metod
├── 07_media_for_thesis.ipynb                  # 🔴 [R] Generování grafů a vizualizací pro text bakalářské práce
│
├── pyproject.toml                             # Konfigurace projektu a závislosti
├── README.md                                  # Dokumentace projektu
└── uv.lock                                    # Uzamčené verze závislostí (pro uv)
```
- 🟢 [Z] (Základní verze): Skript je plně spustitelný i se základní datovou sadou.

- 🔴 [R] (Rozšířená verze): Ke spuštění skriptu jsou potřeba soubory z rozšířené verze přílohy. V případě notebooků `05_results_comparison.ipynb`, `06_ensemble_of_ensembles.ipynb` a `07_media_for_thesis.ipynb` lze tyto chybějící soubory případně vygenerovat také spuštěním kódu v `04_model_train_test_results.ipynb`.