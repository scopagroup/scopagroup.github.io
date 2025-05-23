# Step-by-Step Guide: Install LaTeX (BasicTeX) Without Admin Rights on macOS

To install **LaTeX without admin rights** on macOS, the best option is to use the **BasicTeX** distribution and install it in your **home directory**. Here’s a fully working approach that avoids the need for administrator privileges.

---


### 1. **Download BasicTeX**

Download the latest BasicTeX `.pkg` file from:
[https://www.tug.org/mactex/morepackages.html](https://www.tug.org/mactex/morepackages.html)

### 2. **Extract the .pkg File Manually**

Open a terminal and run the following:

```bash
cd ~/Downloads
pkgutil --expand BasicTeX.pkg ./basictex-expanded
```

This will create a folder `basictex-expanded` with the internal package files.

---

### 3. **Extract the Payload to Your Home Directory**

Now install BasicTeX into your home directory:

```bash
mkdir -p ~/basictex
cd ~/basictex
tar -xvf ~/Downloads/basictex-expanded/BasicTeX.pkg/Payload
```

This places everything inside `~/basictex/usr/local/texlive/...`.

---

### 4. **Update Your Shell Configuration**

Add the binary directory to your `PATH`. Run:

```bash
echo 'export PATH="$HOME/basictex/usr/local/texlive/2024basic/bin/universal-darwin:$PATH"' >> ~/.zshrc
source ~/.zshrc  # or source ~/.bash_profile if using bash
```

---

### 5. **Test Your LaTeX Setup**

Check if it works:

```bash
which pdflatex
pdflatex --version
```

---

### 6. **Install LaTeX Packages (Optional)**

Use the included `tlmgr` (TeX Live Manager) to install missing LaTeX packages:

```bash
tlmgr option repository https://mirror.ctan.org/systems/texlive/tlnet
tlmgr install amsmath latexmk geometry  # example packages
```

> If `tlmgr` gives permission errors, initialize the user tree:

```bash
tlmgr init-usertree
```

---


