# EST — Tradução PT-BR
### Educational Software Tool · Edutec ED08 · Dr.Luck

> Tradução comunitária não oficial do EST para **Português (Brasil)**.  
> Inclui arquivos traduzidos, documentação técnica e pesquisa de engenharia reversa.

---

## O que é o EST?

O **EST (Educational Software Tool)** é um ambiente de programação visual baseado em blocos para robótica educacional, desenvolvido pela **Guangdong Dr.Luck Education Equipment Co., Ltd.** e distribuído no Brasil com o kit **Edutec ED08**.

A arquitetura do software é inspirada no LEGO Mindstorms EV3-G:

| Categoria | Prefixo | Descrição |
|---|---|---|
| Ação | `1xxx` | Motores, saídas |
| Controle de Fluxo | `2xxx` | Loops, condições |
| Sensor | `3xxx` | Leituras de sensores |
| Operações de Dados | `4xxx` | Variáveis, cálculos |
| Avançado | `5xxx` | Funções, comunicação |

Os blocos são definidos por **38 arquivos XML** localizados em `EST/module_xml`, nomeados no formato `X0YY.xml` (onde `X` = categoria e `YY` = posição do bloco).

---

## Estado da Tradução

| Componente | Status |
|---|---|
| Blocos (`module_xml`) | ✅ Traduzido |
| Nomes e modos dos blocos | ✅ Traduzido |
| Labels e tooltips dos parâmetros | ✅ Traduzido |
| Menus internos dos blocos | ✅ Traduzido |
| Tela "Sobre" | ✅ Traduzido (v1.0a) |
| Barra de menus (`File`, `Edit`, `Tools`, `Help`) | 🔄 Parcial |
| Mensagens internas e diálogos | 🔄 Em pesquisa |
| Firmware Update / Import Brick Program | 🔄 Em pesquisa |

---

## Como Instalar

1. Baixe o `.zip` da [última release](../../releases/latest)
2. Extraia o conteúdo em qualquer pasta
3. Abra o EST normalmente pelo `maintest.exe`

> O `.zip` contém a **pasta completa do programa já traduzida** — não é necessário ter o EST instalado previamente.  
> Caso você já tenha uma instalação, faça backup da pasta original antes de substituir.

---

## Estrutura do Repositório

```
EST-Edutec-ED08---Dr.Luck/
│
├── images/
│   └── releases/          # Screenshots das releases
│
├── LICENSE
└── README.md
```

> Os arquivos patchados são distribuídos via [Releases](../../releases).

---

## Detalhes Técnicos

O EST é uma aplicação **Qt/C++** (Qt5). As DLLs presentes na instalação incluem:

```
Qt5Core.dll · Qt5Gui.dll · Qt5Widgets.dll · Qt5Xml.dll · Qt5Network.dll
```

### Por que a tradução é complexa?

- Não há arquivos `.qm` externos — as strings da interface estão compiladas dentro do `maintest.exe`
- Não foi encontrado uso de `QTranslator` para carregamento externo de traduções
- A interface apresenta uma mistura de **inglês**, **chinês** e **traduções parciais anteriores**
- Os textos dos blocos ficam nos XMLs (editáveis), mas menus e diálogos exigem **edição hexadecimal** do executável

### Ferramentas utilizadas

| Ferramenta | Uso |
|---|---|
| **HxD** | Edição hexadecimal do executável |
| **Resource Hacker** | Inspeção de recursos PE |
| **Edição manual de XML** | Tradução dos blocos |

---

## Contribuindo

Contribuições são bem-vindas! Você pode ajudar com:

- Identificar strings em chinês ou inglês ainda não traduzidas
- Testar o patch em diferentes versões do kit Edutec
- Sugerir melhorias nas traduções existentes
- Documentar descobertas de engenharia reversa

Abra uma [Issue](../../issues) ou envie um [Pull Request](../../pulls).

---

## Aviso Legal

Este projeto **não possui vínculo com a Guangdong Dr.Luck Education Equipment Co., Ltd.**  
Todos os direitos do software original pertencem aos seus respectivos proprietários.

O objetivo deste repositório é exclusivamente **educacional**, de **preservação de software** e **localização para a comunidade brasileira de robótica**.

---

## Licença

Os arquivos de documentação, pesquisas e traduções produzidos para este projeto podem ser utilizados livremente para fins educacionais.
O software EST original continua pertencendo à Guangdong Dr.Luck Education Equipment Co., Ltd. e aos seus respectivos detentores de direitos.

Este repositório não reivindica propriedade sobre o software original.
