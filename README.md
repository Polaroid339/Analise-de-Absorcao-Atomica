# 🔬 Análise de Absorção Atômica

Este projeto é uma aplicação web progressiva projetada para laboratórios de análise mineral e química. Ele automatiza o processo de registro, cálculo e geração de laudos para análises de Absorção Atômica e Ensaios Granulométricos, substituindo planilhas complexas por uma interface intuitiva e moderna.

![Versão](https://img.shields.io/badge/versão-5.0.0-indigo)
![Tecnologias](https://img.shields.io/badge/stack-React%20%7C%20Tailwind%20%7C%20Lucide-blue)
![Licença](https://img.shields.io/badge/licença-MIT-green)

## ✨ Funcionalidades Principais

-   **🧪 Gestão de Análises Químicas:**
    -   Suporte para elementos como Cobre (Cu), Zinco (Zn) e Chumbo (Pb).
    -   Métodos de digestão configuráveis (Água Régia, HCl).
    -   Cálculo automático de **Teor (%)** baseado em Peso da Amostra, Volume Final, Fator de Diluição e Médias de Leitura (ppm).
    -   Entrada dinâmica de múltiplas leituras (duplicatas/triplicatas) com média em tempo real.

-   **⚖️ Análise Granulométrica:**
    -   Cálculo de rendimento por malhas (Retido #35, Retido #60 e Passante).
    -   Cálculo automático de porcentagem de massa e massa total.

-   **📊 Gestão de Dados:**
    -   **Pesquisa Inteligente:** Filtre laudos por ID, Cliente ou Lote.
    -   **Persistência Local:** Os dados são salvos automaticamente no navegador (LocalStorage).
    -   **Exportação Excel:** Gere planilhas `.xlsx` com todos os dados consolidados.
    -   **Backup/Restauração:** Exporte e importe todo o banco de dados em formato `.json`.
    -   **Cópia Rápida:** Formatação exclusiva para compartilhamento de resultados via WhatsApp/Telegram.

-   **🖨️ Design Impressionista & Print-Ready:**
    -   Interface moderna com Tailwind CSS.
    -   Layout de impressão otimizado (remove botões e elementos desnecessários ao imprimir o laudo).

## 🚀 Como Executar

O projeto foi construído para ser extremamente portável, rodando diretamente no navegador sem a necessidade de instalar dependências complexas (Node.js/NPM) para uso básico, utilizando CDNs para React e Tailwind.

1.  Faça o download do arquivo `index.html`.
2.  Abra o arquivo em qualquer navegador moderno (Chrome, Edge, Firefox).
3.  Pronto! A aplicação está pronta para uso.


## 🛠️ Tecnologias Utilizadas

-   **Frontend:** [React.js](https://reactjs.org/) (via ESM)
-   **Estilização:** [Tailwind CSS](https://tailwindcss.com/)
-   **Ícones:** [Lucide React](https://lucide.dev/)
-   **Manipulação de Dados:** [SheetJS (XLSX)](https://sheetjs.com/)
-   **Compilação Runtime:** [Babel Standalone](https://babeljs.io/)

## 📝 Estrutura de Dados (JSON)

Ao realizar um backup, o arquivo gerado segue esta estrutura:

```json
[
  {
    "id": "uuid",
    "customId": "101",
    "clientName": "Nome do Cliente",
    "batchNumber": "Lote 2024",
    "process": "Flotação",
    "showGranulometry": true,
    "meshData": {
      "retained35g": 1.5,
      "retained60g": 0.5,
      "passingG": 8.0
    },
    "entries": [
      {
        "element": "Cu",
        "digestion": "Regia",
        "sampleWeight": 1.0,
        "finalVolume": 100,
        "dilutionFactor": 1,
        "readings": [15.2, 15.4],
        "finalPercentage": 0.153
      }
    ],
    "photos": []
  }
]
```

## 📄 Licença

Este projeto está sob a licença MIT. Consulte o arquivo para mais detalhes.

---
*Desenvolvido para otimização de rotinas laboratoriais.*
