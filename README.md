# G-Earth - Portable Distribution (Unofficial)

[![Original Repository](https://img.shields.io/badge/Original_Repo-sirjonasxx%2FG--Earth-blue)](https://github.com/sirjonasxx/G-Earth)
[![Java Version](<https://img.shields.io/badge/Java-8_Full_(BellSoft)-red>)](https://bell-sw.com/)

[🇧🇷 Português](#-versão-em-português) | [🇺🇸 English](#-english-version)

---

## 🇧🇷 Versão em Português

Esta é uma distribuição customizada e "Portable" (Portátil) do **G-Earth 1.5.3**, criada para facilitar a execução em computadores modernos que não possuem o Java configurado ou que enfrentam problemas com o JavaFX.

Este projeto baseia-se inteiramente no incrível trabalho de [sirjonasxx](https://github.com/sirjonasxx). O objetivo deste repositório não é alterar o código-fonte do G-Earth, mas sim fornecer um ambiente de execução (Runtime) que garanta seu funcionamento.

### 📌 O Problema

O G-Earth depende de uma biblioteca gráfica chamada **JavaFX**. Nas versões modernas do Java (e em muitas instalações padrão do Windows), essa biblioteca foi removida, fazendo com que o G-Earth não abra ou apresente erros como `ClassNotFoundException`.

### 🛠 A Solução Técnica

Para corrigir isso sem obrigar o usuário a desinstalar ou modificar seu Java atual, esta distribuição inclui:

1.  **Java Embutido (BellSoft Liberica JDK 8 Full)**: Uma versão completa do Java que fica dentro da pasta `jre`. Ela já contém o JavaFX nativamente.
2.  **Isolamento**: O sistema não usa o Java instalado no seu Windows. Ele usa apenas a versão que está dentro da pasta, garantindo que "funcione em qualquer lugar".
3.  **Bootstrapper (`Iniciar G-Earth.bat`)**: Um script especial que forçam o G-Earth a usar o nosso Java embutido.

### 🚀 Como Usar

1.  Baixe este repositório.
2.  Execute o arquivo **`Iniciar G-Earth.bat`**.
    - _Nota: Não use o `G-Earth.exe` original, pois ele tentará usar o Java do seu sistema, que provavelmente não funcionará._

### 📂 Estrutura de Arquivos

- `Iniciar G-Earth.bat`: **Use este arquivo para abrir.**
- `jre/`: Pasta contendo o Java Portátil (não apague).
- `Extensions/`: Pasta onde você pode colocar suas extensões do G-Earth.

---

## 🇺🇸 English Version

This is a custom "Portable" distribution of **G-Earth 1.5.3**, designed to facilitate execution on modern computers that lack a compatible Java configuration or face issues with JavaFX.

This project is entirely based on the amazing work by [sirjonasxx](https://github.com/sirjonasxx). The goal of this repository is not to modify G-Earth's source code, but to provide a cohesive Runtime Environment ensuring it works out-of-the-box.

### 📌 The Problem

G-Earth relies on the **JavaFX** graphics library. In modern Java versions (and many standard Windows installations), this library has been decoupled, causing G-Earth to fail at startup with errors like `ClassNotFoundException`.

### 🛠 The Technical Solution

To fix this without forcing the user to uninstall or modify their system-wide Java, this distribution includes:

1.  **Embedded Java (BellSoft Liberica JDK 8 Full)**: A complete Java Runtime located in the `jre` folder. It natively includes the required JavaFX binaries.
2.  **Isolation**: This system does not use the Java installed on your Windows OS. It exclusively uses the enclosed version, ensuring a "Write Once, Run Anywhere" experience.
3.  **Bootstrapper (`Iniciar G-Earth.bat`)**: A specialized batch script that forces G-Earth to launch using our embedded Java runtime.

### 🚀 How to Use

1.  Download this repository.
2.  Run the **`Iniciar G-Earth.bat`** file.
    - _Note: Do not use the original `G-Earth.exe`, as it will attempt to use your system's Java, which likely won't work._

### 📂 File Structure

- `Iniciar G-Earth.bat`: **Run this file to start the application.**
- `jre/`: Folder containing the Portable Java Runtime (do not delete).
- `Extensions/`: Folder where you can drop your G-Earth extensions.

---

**All credits for the G-Earth software go to [sirjonasxx](https://github.com/sirjonasxx).**
**This repository maintains the "Portable Setup" wrapper.**
