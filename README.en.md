# 📚Quantum Physics Notes - A.A. 2026/2027

[🇮🇹 Leggi in italiano](README.md)

Welcome to the shared repository of the Quantum Physics course notes! Here we collect, write in **LaTeX** and update the lecture material together.

---

## 🛠️ 1. Initial Installation and Configuration (First time only)

To write and compile the notes on your computer you need to install **Git**, **Visual Studio Code** and a **LaTeX compiler**. Follow the step-by-step guide for your operating system.

---

### 🪟 GUIDE FOR WINDOWS

#### Step 1.1: Install Git

1. Go to the official Git website: [git-scm.com/download/win](https://git-scm.com/download/win).
​2. The download should start automatically (or click on *Click here to download manually* if you use 64-bit versions).
2. Open the downloaded file (`.exe`) and click on **Next (Avanti)** in all screens, leaving the recommended default settings active.

#### Step 1.2: Install Visual Studio Code (VS Code)

1. Go to the official website: [code.visualstudio.com](https://code.visualstudio.com/).
​2. Click on the large blue **Download for Windows** button to download the installer.
2. Open the downloaded executable file. During installation:
* Accept the license conditions.
* Make sure to check the box **"Add 'Open with Code' to Windows context menu"** and **"Add to PATH"** (so the computer will recognize VS Code everywhere).
* Click on **Install** and then on *Finish*.



#### Step 1.3: Install the LaTeX compiler (MiKTeX + Strawberry Perl)

To compile `.tex` files on Windows you need MiKTeX (the LaTeX engine) and Strawberry Perl (necessary for VS Code to automate the PDF generation):

1. **Install MiKTeX:**
* Go to [miktex.org/download](https://miktex.org/download) and download the installer for Windows.
* Launch it, accept the terms and select *Install MiKTeX only for me* (or for all users).
* In the missing packages screen, select **Yes** for the item *"Install missing packages on-the-fly"* (it will avoid errors if you use particular packages). When finished, close the installation.


2. **Update MiKTeX:**
* Open the Windows Start menu, search for and open **MiKTeX Console**.
* Click on **Updates** in the left menu, then on **Check for updates**. If there are updates, click on **Update now**.


3. **Install Strawberry Perl (MANDATORY for Windows):**
* Go to [strawberryperl.com](https://strawberryperl.com/).
* Download the recommended 64-bit version (`.msi` installer).
* Open the downloaded file and click on *Next* until the installation is complete.


4. **Restart the computer** to make the changes effective.

---

### 🍎 GUIDE FOR MAC (macOS)

#### Step 1.1: Install Git

1. Open the **Terminal** app on the Mac (press `Cmd + Space`, type "Terminal" and press Enter).
​2. Type the command `git --version` and press Enter.
2. If Git is not installed, macOS will automatically open a window asking you to install the *Command Line Tools*. Click on **Install** and wait for the download to finish.

#### Step 1.2: Install Visual Studio Code (VS Code)

1. Go to the official website: [code.visualstudio.com](https://code.visualstudio.com/).
​2. Click on the download button for Mac (select the *Universal* version or the specific one for your Apple Silicon / Intel processor).
2. Open the *Downloads* folder and drag the **Visual Studio Code** icon into the **Applications** folder.

#### Step 1.3: Install the LaTeX compiler (MacTeX)

On Mac there is a complete package that includes everything needed without additional configurations:

1. Go to the MacTeX website: [tug.org/mactex/mactex-download.html](https://tug.org/mactex/mactex-download.html).
​2. Click on the **`MacTeX.pkg`** link to start the download (it's a heavy file, about 5 GB, because it already includes all the math symbol and font packages).
2. Once the download is complete, open the `.pkg` file and follow the installation wizard by always clicking on *Continue* and entering the Mac password when requested. *(Note: on macOS Perl support is already natively integrated into the system).*

---

### ⚙️ Configure VS Code (Valid for Windows and Mac)

Once all programs are installed, open **Visual Studio Code** and complete these final steps:

1. **Install the LaTeX Workshop extension:**
* Click on the **Extensions** icon in the left sidebar (the four squares, or press `Ctrl + Shift + X` on Windows / `Cmd + Shift + X` on Mac).
* Type **`LaTeX Workshop`** (developed by *James Yu*) and click on **Install**.


2. **Configure Git with your name and your email:**
* From the top menu of VS Code select **Terminal** -> **New Terminal**.
* In the terminal panel at the bottom, paste these two commands (replacing the data in quotes with your real name and the email associated with your GitHub account) and press Enter after each one:
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

```




3. **Connect your GitHub account to VS Code:**
* Click on the **Profile** icon (gear or little person at the bottom left in the VS Code sidebar).
* Click on **Sign in with GitHub to use...** and authorize access via the browser page that will open automatically.



---

## 📥 2. How to download the Repository on VS Code (Cloning)

1. Open VS Code.
​2. Press `Ctrl + Shift + P` (on Windows) or `Cmd + Shift + P` (on Mac) to open the command bar at the top.
2. Type **`Git: Clone`** and press Enter.
3. Select **Clone from GitHub** (or paste the URL of this web page directly).
4. Select the repository from the list that appears and choose an empty folder on your computer in which to save it.
5. When VS Code asks you in the bottom right if you wish to open the cloned folder, click on **Open**.

---

## 📄 3. How the LaTeX files are organized and how to compile the PDF

To prevent two people from modifying the same file at the same time creating conflicts, the notes are organized in this way:

* **`main.tex`**: is the main file. It contains only the graphic setting, the packages (`\usepackage`), the index and the references to the individual lectures (`\input{lezioni/lezioneXX.tex}`). **Do not write the notes directly in here.**
* **`lezioni/` folder**: contains a separate file for each lecture (e.g. `lezione01.tex`, `lezione02.tex`). In here only the text of the lecture must be written (starting directly from `\section{...}`), **without** putting back `\documentclass` or `\begin{document}`.
* **`immagini/` folder**: contains all the images or diagrams referenced in the notes.

### How to generate and see the PDF on VS Code:

1. When you write and save a `.tex` file (`Ctrl + S` on Windows / `Cmd + S` on Mac), *LaTeX Workshop* will start the automatic compilation in the background.
​2. To see the PDF preview side by side with the code, open the `main.tex` file and click on the **View LaTeX PDF** icon at the top right (the sheet with the magnifying glass). Choose whether to view it in an internal VS Code tab or in the browser.
2. *Important note:* The final compiled PDF file (`main.pdf`) remains saved only on your computer to allow you to read the preview; it is automatically ignored by Git (thanks to the `.gitignore` file set to `TeX`) to avoid conflicts and blocks during synchronization with colleagues.

---

## 🔄 4. How to work together (Daily workflow)

To avoid overwriting the work of others, **always** follow these 4 steps in the exact order every time you open VS Code to study or add notes:

### Step A: Download others' changes (`Pull`) — *ALWAYS DO IT BEFORE STARTING*

Before writing any line of text, make sure you have the latest updated version:

1. Click on the **Source Control** icon in the left bar (the one with the three dots connected by lines, or press `Ctrl + Shift + G`).
​2. Click on the three dots **`...`** at the top in the Source Control panel -> **Pull**. *(Alternatively, you can click on the circular synchronization arrows icon at the bottom left in the status bar).*

### Step B: Write or edit the notes

* Open the file of the lecture you need to work on (inside the `lezioni/` folder) or create a new one and add it in `main.tex` via the `\input{lezioni/nomefile.tex}` command.
* Save the file (`Ctrl + S` or `Cmd + S`) and check from the PDF panel that the compilation happens without errors.

### Step C: Record your local changes (`Commit`)

When you have finished writing or fixing a lecture:

1. Go back to the **Source Control** panel on the left: you will see the list of modified files under the *Changes* heading.
​2. Hover the mouse over the *Changes* heading and click on the **`+`** symbol (*Stage All Changes*) to add the files ready for saving.
2. In the **Message** text box at the top, write a short but clear message that explains what you did (e.g. `Added lecture 04 notes on matrices and vectors`).
3. Click on the large blue **Commit** button.

### Step D: Send the changes online (`Push`)

1. Immediately after doing the Commit, the blue button will change label to **Sync Changes** (or **Push**). Click on it.
​2. Your changes will be uploaded to the online GitHub repository, ready to be downloaded by your colleagues.

---

## 🌿 5. Working on major changes without doing damage (Branch)

If you or a colleague have to do a deep revision, reorganize the chapters or write many test pages, **do not work directly on the main branch (`main`)**, but create a separate branch:

1. Click on the name of the current branch (usually **`main`**) that you see at the bottom left in the VS Code status bar.
​2. In the drop-down menu that appears at the top, select **+ Create new branch...**.
2. Give it a descriptive name without spaces (e.g. `analysis-revision` or `added-exercises`) and press Enter.
3. Work normally doing your *Commits* and *Pushes* on this new branch (clicking on *Publish Branch* the first time).
4. When the work is complete and verified, go to the GitHub web page of the repository and open a **Pull Request** to safely merge your branch to the `main`.

---

## ⚖️ License

This work is distributed under a **[Creative Commons Attribution - NonCommercial - ShareAlike 4.0 International License (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.it)**.

* **You are free to:** share, copy and redistribute the material in any medium or format for any non-commercial purpose.
* **Under the following terms:** you must give appropriate credit to the original authors, indicate if changes were made, you may not use the material for commercial purposes and, if you remix, transform or build upon the material, you must distribute your contributions under the exact same license as the original material.
