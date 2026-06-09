# 2D Molecule Editor & InChIKey Generator

A lightweight, purely client-side web application that allows users to draw chemical structures in 2D and instantly generate their corresponding chemical identifiers (**SMILES** and **InChIKey**).

## 🚀 Live Demo
[https://petrusen.github.io/getinchi/]

## 🛠️ How it Works
This repository hosts a single self-contained web page (`index.html`). Because it runs completely in the browser without requiring a backend server, it can be deployed instantly to GitHub Pages.

It bridges two powerful open-source chemistry libraries via CDN:
* **Kekule.js**: Provides the interactive 2D molecule editor canvas and UI tools.
* **RDKit.js (WebAssembly)**: Serves as the underlying cheminformatics engine to validate the molecule structure and compute the canonical SMILES string and cryptographic InChIKey hash.

## 💻 How to Use Locally
1. Clone or download this repository.
2. Because RDKit.js utilizes WebAssembly, modern browsers block it from running via direct file opening (`file://`). You must serve it via a local web server.
3. Open your terminal in the project folder and run:
   ```bash
   python -m http.server 8000
