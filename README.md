# 2D structure ⇄ SMILES/InChIKey

A lightweight, purely client-side web application that allows users to seamlessly convert between 2D chemical structures and molecular identifiers (**SMILES** and **InChIKey**).

## 🚀 Live Demo
[https://petrusen/getinchi/]

## 🛠️ How it Works
This repository hosts a single self-contained web page (`index.html`). Because it runs completely in the browser without requiring a backend server, it can be deployed instantly to GitHub Pages.

It bridges two powerful open-source chemistry libraries via CDN:
* **Kekule.js**: Provides the interactive 2D molecule editor canvas and UI tools.
* **RDKit.js (WebAssembly)**: Serves as the underlying cheminformatics engine to generate canonical SMILES/InChIKeys from 2D structures, and to generate coordinate tables to render 2D structures back from raw SMILES strings.

## 🔒 Privacy & Security
Molecular data and input strings provided by users **are not transmitted, tracked, or stored on any server**. All computations run strictly client-side within your browser's temporary memory.

## 💻 How to Use Locally
1. Clone or download this repository.
2. Because RDKit.js utilizes WebAssembly, modern browsers block it from running via direct file opening (`file://`). You must serve it via a local web server.
3. Open your terminal in the project folder and run:
   ```bash
   python -m http.server 8000
