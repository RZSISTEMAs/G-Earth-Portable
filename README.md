# G-Earth - Portable Setup (Legacy Java Fix)

Este repositório contém uma distribuição "Portable" otimizada do **G-Earth 1.5.3**, configurada especificamente para contornar problemas de compatibilidade com ambientes modernos que não possuem bibliotecas legadas do JavaFX.

## 📋 Visão Geral Técnica

O software original (G-Earth) depende do JavaFX, que foi desacoplado do JDK padrão nas versões mais recentes (Java 11+ e algumas builds do 8). Isso resulta no erro `ClassNotFoundException: gearth.GEarth` ou falhas silenciosas ao tentar iniciar o executável padrão em máquinas não preparadas.

Esta distribuição resolve o problema via **Vendor-Locking** da JRE (Java Runtime Environment), garantindo que o software execute em um ambiente isolado e controlado, independente das variáveis de ambiente do sistema operacional do usuário.

## 🛠 Alterações Realizadas

1.  **Inclusão de Runtime Dedicado (JRE)**:
    - Foi integrado o **BellSoft Liberica JDK 8 Full Edition**.
    - Esta versão específica inclui o JavaFX (`jfxrt.jar`), que é pré-requisito mandatório para a interface gráfica do G-Earth.
    - _Nota_: A JRE está localizada em `./jre` e é totalmente independente da instalação do sistema.

2.  **Script de Inicialização Personalizado (`Iniciar G-Earth.bat`)**:
    - Substituição da chamada de sistema padrão.
    - O script força o uso do binário local `./jre/bin/java.exe`.
    - Argumentos de classpath definidos explicitamente para garantir o carregamento das dependências.

## 🚀 Como Executar

Não é necessário instalar Java no computador.

1.  Clone este repositório ou baixe o ZIP.
2.  Execute o arquivo:
    ```bash
    Iniciar G-Earth.bat
    ```

## 📁 Estrutura do Projeto

```text
.
├── Dependencies/       # Bibliotecas de terceiros requeridas pelo G-Earth
├── Extensions/         # Diretório reservado para Extensões do usuário
├── jre/                # Java Runtime Environment (Portable Full JDK 8)
├── G-Earth.jar         # Core Application Assembly
├── G-Earth.exe         # Wrapper legado (não recomendado usar este)
└── Iniciar G-Earth.bat # Script de execução corrigido (EntryPoint Recomendado)
```

## ⚠️ Notas de Desenvolvimento

- **Versão do G-Earth**: 1.5.3 (Stable)
- **Versão do Java Embutida**: 1.8.0_282 (Liberica Full)
- **Arquitetura**: Windows x64

---

_Este setup foi criado para garantir estabilidade e facilidade de uso em ambientes de desenvolvimento Windows._
