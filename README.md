# Gradientní boosting rozhodovacích stromů - Gradient Boosting of Decision Trees

Tento repozitář obsahuje kód a Jupyter notebooky pro mou bakalářskou práci. Pro správu závislostí se používá nástroj [uv](https://github.com/astral-sh/uv).

## Jak projekt zprovoznit (pro Visual Studio Code)

1. **Nainstalujte si nástroj `uv` (pokud nemáte již instalováno)**:
   - Viz [oficiální návod](https://docs.astral.sh/uv/getting-started/installation/) nebo pomocí curl:
     ```bash
     curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh
     ```

2. **Získejte zdrojové kódy**:

   **Varianta A: Stažení přílohy práce**
   - Rozbalte stažený archiv s přílohou.
   - Otevřete terminál v rozbalené složce.

   **Varianta B: Klonování z GitHubu**
   - Spusťte následující příkazy:
     ```bash
     git clone [https://github.com/oskarklima/bachelor_thesis](https://github.com/oskarklima/bachelor_thesis)
     cd bachelor_thesis
     ```

3. **Nainstalujte závislosti a vytvořte prostředí**:

   Tento příkaz automaticky vytvoří složku `.venv` a nainstaluje verze balíčků, které zaručují funkčnost kódu (podle `uv.lock`).

   ```bash
   uv sync --frozen
   ```

4. **Spuštění ve Visual Studio Code**:
   - Otevřete tuto složku ve VS Code.
   - Otevřete libovolný `.ipynb` soubor.
   - Vpravo nahoře klikněte na **Select Kernel** → **Python Environments** a vyberte prostředí ze složky `.venv`.

------

This repository contains the code and Jupyter notebooks for my bachelor's thesis. The [uv](https://github.com/astral-sh/uv) tool is used for dependency management.

## Setup Instructions (for Visual Studio Code)

1. **Install `uv` (if not already installed)**:
   - Refer to the [official documentation](https://docs.astral.sh/uv/getting-started/installation/) or use curl:
     ```bash
     curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh
     ```

2. **Get the Source Code**:

   **Option A: Downloaded Thesis Attachment**
   - Extract the downloaded archive containing the thesis files.
   - Open your terminal in the extracted folder.

   **Option B: Clone from GitHub**
   - Run the following commands:
     ```bash
     git clone [https://github.com/oskarklima/bachelor_thesis](https://github.com/oskarklima/bachelor_thesis)
     cd bachelor_thesis
     ```

3. **Install Dependencies and Create Environment**:

   This command automatically creates a `.venv` folder and installs package versions required to ensure the code runs correctly (based on `uv.lock`).

   ```bash
   uv sync --frozen
   ```

4. **Running in Visual Studio Code**:

   - Open this folder in VS Code.
   - Open any `.ipynb` file.
   - In the top right corner, click **Select Kernel** → **Python Environments** and select the environment from the `.venv` folder.