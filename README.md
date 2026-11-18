# 💊 Bulex Plus

Entrega Final: 23 de Novembro de 2026.
Versão atualizada de um aplicativo de leitura de bulas de medicamentos via QR Code, desenvolvido ao longo do ano de 2026 para a disciplina de Projeto Integrador, do curso de Análise e Desenvolvimento de Sistemas do Senac.

Vídeo de apresentação do Bulex: "EM BREVE"


```
# GRUPO 02
├── Amaury Serpa Santos Neto
├── Diego Paladini Machado
├── Diogo Oliveira Rodrigues
├── Erika Kívia Santos Barbosa
├── Murilo Luzzi Do Couto
├── Ricardo Bertoldo
```
> ⚠️ **Aviso importante:** o Bulex Plus é um **protótipo acadêmico**, criado para a disciplina de Projeto Integrador. As informações exibidas **não substituem** a bula oficial do medicamento nem a orientação de um médico ou farmacêutico. Em caso de dúvida sobre o uso de qualquer medicamento, procure um profissional de saúde. Em caso de emergência, ligue para o SAMU (192).
---

## 📱 Como testar em 1 minuto

Acesse o app publicado: **https://bulex-mvp.onrender.com**

> ⏳ O app está hospedado no plano gratuito do Render. Se ficar um tempo sem acesso, o **primeiro carregamento pode levar até 1 minuto**. Depois disso, fica rápido.

### Opção 1: Escanear pelo app (experiência real).

Reproduz o Sr. João apontando a câmera para o QR Code da embalagem do remédio. Os QR Codes abaixo fazem o papel das embalagens.

1. Deixe esta página do README aberta na tela do computador.
2. No celular, abra **https://bulex-mvp.onrender.com** e toque em **"Escanear QR Code"**.
3. Permita o uso da câmera quando o navegador pedir.
4. Aponte para um dos QR Codes abaixo. A bula abre sozinha, sem digitar nada.
5. Toque em **"Ler a bula completa"** para ver todas as informações.

> 💡 Também funciona com a webcam do computador (mostrando o QR Code no celular) ou apontando a câmera comum do celular, fora do app, para o QR Code

<table>
  <tr>
    <td align="center">
      <img src="docs/qrcodes/medicamento-1.png" width="170" alt="QR Code do medicamento 1 - Losartana Potássica"><br>
      <b>1</b> · Losartana Potássica
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-2.png" width="170" alt="QR Code do medicamento 2 - Amoxicilina"><br>
      <b>2</b> · Amoxicilina
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-3.png" width="170" alt="QR Code do medicamento 3 - Dipirona"><br>
      <b>3</b> · Dipirona
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-4.png" width="170" alt="QR Code do medicamento 4 - Metformina"><br>
      <b>4</b> · Metformina
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-5.png" width="170" alt="QR Code do medicamento 5 - Atenolol"><br>
      <b>5</b> · Atenolol
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="docs/qrcodes/medicamento-6.png" width="170" alt="QR Code do medicamento 6 - Sinvastatina"><br>
      <b>6</b> · Sinvastatina
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-7.png" width="170" alt="QR Code do medicamento 7 - Omeprazol"><br>
      <b>7</b> · Omeprazol
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-8.png" width="170" alt="QR Code do medicamento 8 - Paracetamol"><br>
      <b>8</b> · Paracetamol
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-9.png" width="170" alt="QR Code do medicamento 9 - Tramadol"><br>
      <b>9</b> · Tramadol
    </td>
    <td align="center">
      <img src="docs/qrcodes/medicamento-10.png" width="170" alt="QR Code do medicamento 10 - Famotidina"><br>
      <b>10</b> · Famotidina
    </td>
  </tr>
</table>

### Opção 2: Digitar o número (sem câmera)

1. Abra **https://bulex-mvp.onrender.com**.
2. Em **"ou digite o número"**, informe o número de um medicamento (de **1 a 10**, conforme a tabela acima) e clique em **"Abrir bula"**.
3. Para ver a tela de erro, digite um número que não existe, como **99**.

---

## 🎯 Jornada do Usuário

**Persona:** Sr. João, 67 anos, é um paciente hipertenso que acaba de receber uma nova prescrição em uma consulta ambulatorial. Ele tem dificuldade com termos técnicos e letras pequenas

**Problema:** Bulas de medicamentos são complicadas de ler (letra pequena, linguagem técnica, informações desorganizadas em resumo ou informações extensas; alguns laboratórios não dão a importância necessária às bulas).

**Solução:** O usuário escaneia o QR Code da embalagem e recebe as informações do medicamento de forma clara, acessível e com tipografia ampliada.

---

## 🛠️ Tecnologias Utilizadas

| Camada         | Tecnologia                                         |
| -------------- | -------------------------------------------------- |
| Front-end      | HTML5, CSS3, JavaScript, Jinja2 Templates          |
| Leitor de QR   | html5-qrcode (leitura pela câmera, no navegador)   |
| Back-end       | Python 3, FastAPI                                  |
| Banco de Dados | SQLite3                                            |
| Servidor       | Uvicorn (ASGI)                                     |
| Hospedagem     | Render (plano gratuito)                            |

---

## 📁 Estrutura do Projeto

```
bulex_plus/
├── main.py              # Aplicação FastAPI (rotas e lógica)
├── database.py          # Criação e seed do banco de dados
├── requirements.txt     # Dependências Python
├── scripts/
│   └── gerar_qrcodes.py # Gera os QR Codes de docs/qrcodes (uso em desenvolvimento)
├── docs/
│   └── qrcodes/         # QR Codes de cada medicamento (usados neste README)
├── bulex.db             # Banco de dados SQLite (gerado automaticamente, não versionado)
├── dados/
│   └── bulas.json       # Conteúdo da bula completa de cada medicamento
└── templates/
    ├── base.html            # Layout e paleta de cores compartilhados
    ├── index.html           # Tela inicial (leitor de QR Code pela câmera)
    ├── bula.html            # Resumo da bula
    ├── bula_completa.html   # Bula completa (modelo de bula para o paciente da Anvisa)
    └── nao_encontrado.html  # Tela de medicamento não encontrado
```

---

## ▶️ Como Rodar o Projeto

### Pré-requisitos

- Python 3.10+
- pip

### Instalação

```bash
# Clone o repositório
git clone https://github.com/diegopalladini/bulex_plus.git
cd bulex_plus

# Crie e ative o ambiente virtual
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate

# Instale as dependências
pip install -r requirements.txt
```

### Executando

```bash
uvicorn main:app --reload
```

O banco de dados (`bulex.db`) é criado e preenchido automaticamente quando o servidor inicia.

Acesse no navegador: **http://127.0.0.1:8000**

(ou na web: **https://bulex-mvp.onrender.com**)

---

## 🗺️ Rotas da API

| Método | Rota | Descrição |
|--------|------|-----------|
| GET | `/` | Tela inicial (leitor de QR Code pela câmera) |
| GET | `/medicamento/{id}` | Exibe o resumo da bula do medicamento pelo ID |
| GET | `/medicamento/{id}/bula` | Exibe a bula completa do medicamento |

---

## 💾 Modelagem de Dados

**Tabela: `medicamentos`**

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `id` | INTEGER (PK) | Identificador único |
| `nome` | TEXT | Nome do medicamento |
| `finalidade` | TEXT | Para que serve |
| `como_tomar` | TEXT | Posologia |
| `alerta` | TEXT | Sinais de alerta / efeitos colaterais |

**Tabela: `bulas`** (bula completa, carregada de `dados/bulas.json`)

| Coluna | Tipo | Descrição |
|--------|------|-----------|
| `medicamento_id` | INTEGER (PK, FK) | Referência ao medicamento |
| `como_funciona` | TEXT | Como o medicamento age |
| `contraindicacoes` | TEXT | Quando não usar |
| `precaucoes` | TEXT | Cuidados antes de usar |
| `interacoes` | TEXT | Medicamentos e alimentos que interagem |
| `armazenamento` | TEXT | Como guardar |
| `esqueceu_dose` | TEXT | O que fazer se esquecer uma dose |
| `reacoes_adversas` | TEXT | Efeitos colaterais |
| `superdose` | TEXT | O que fazer em caso de dose excessiva |

Os campos em lista no JSON são gravados com um item por linha e exibidos como tópicos.
**Fonte do conteúdo das bulas:** [CONFIRMAR COM O GRUPO, ex.: bulário eletrônico da Anvisa]. Última atualização dos dados: [DD/MM/2026].

**Dados de teste incluídos (10 medicamentos):**
- ID 1 → Losartana Potássica (hipertensão)
- ID 2 → Amoxicilina (infecções)
- ID 3 → Dipirona (dor/febre)
- ID 4 → Metformina (diabetes tipo 2)
- ID 5 → Atenolol (pressão alta/cardíaco)
- ID 6 → Sinvastatina (colesterol)
- ID 7 → Omeprazol (problemas estomacais)
- ID 8 → Paracetamol (dor/febre)
- ID 9 → Tramadol (dor moderada/intensa)
- ID 10 → Famotidina (refluxo, gastrite e úlcera)

---
## 🧪 Roteiro de testes sugerido:

| ID | Cenário | Passos | Resultado esperado |
|---|---|---|---|
| T01 | Abrir bula por QR Code | Escanear o QR Code do medicamento 1 pelo app | Abre o resumo da Losartana Potássica |
| T02 | Abrir bula digitando o número | Digitar 1 em "ou digite o número" e clicar em "Abrir bula" | Abre o resumo do medicamento 1 |
| T03 | Ver a bula completa | No resumo, tocar em "Ler a bula completa" | Exibe todas as informações da bula |
| T04 | Medicamento inexistente | Digitar 99 e clicar em "Abrir bula" | Exibe a tela "medicamento não encontrado" |
| T05 | Todos os medicamentos | Abrir os IDs de 1 a 10 | Todos abrem resumo e bula completa sem erro |
| T06 | Câmera negada | Negar a permissão da câmera | App continua utilizável pela digitação |
| T07 | Primeiro acesso após inatividade | Abrir o link depois de um tempo sem uso | Carrega em até cerca de 1 minuto |


## 📌 Observações

- Este é um protótipo funcional. A leitura de QR Code usa a câmera do aparelho pelo navegador (biblioteca [html5-qrcode](https://github.com/mebjas/html5-qrcode)); a imagem é processada no próprio aparelho e não é enviada ao servidor. A câmera exige HTTPS (ou `localhost`). Também é possível digitar o número do medicamento.
- O banco de dados é criado automaticamente na primeira execução via "lifespan" do FastAPI.
- Fontes grandes e layout amigável para a 3ª idade foram adotados intencionalmente para garantir acessibilidade (persona Sr. João).

## 🧪 Prova de Conceito (POC)

**Objetivo**  
Validar a viabilidade de um sistema que permita o acesso a bulas de medicamentos de forma simplificada e acessível, a partir da leitura de um identificador (simulando QR Code).

**Risco Técnico**  
O principal risco técnico é garantir que o sistema consiga recuperar e exibir corretamente informações dos medicamentos de forma clara e legível para usuários com dificuldades de leitura.

**Hipótese**  
É possível exibir informações de medicamentos de forma mais acessível que a bula tradicional, melhorando a experiência do usuário.

**Resultados**  
- A aplicação foi capaz de recuperar e exibir corretamente os dados dos medicamentos cadastrados.  
- O tempo de resposta da aplicação é imediato (inferior a 1 segundo).  
- A interface apresentou melhor legibilidade em comparação com as bulas tradicionais.

**Limitações**  
- ~~A leitura de QR Code ainda é simulada por um campo de entrada manual.~~ Resolvido no Bulex Plus: leitura real pela câmera.  
- Base de dados expandida com 10 medicamentos comuns, mas pode ser ampliada conforme necessário.  
- Não houve testes com usuários reais.
