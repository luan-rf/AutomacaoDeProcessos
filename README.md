# AutomacaoDeProcessos
Automação de processos em Python - Relatório de vendas (Daily)

Projeto que integra diversas bases de dados de vendas de diversas fontes (que não acompanham este diretório) com o Pandas, realiza o cálculo de indicadores técnicos das vendas, faz a integração de arquivos de forma automática, criando arquivos de backup e novos arquivos com os resultados consolidados após o processo finalizado. A automação também tem vinculo com o e-mail (gmail) encaminhando os resultados para bases de contato de forma automática, editando os dados de forma dinâmica para os contatos em formato de Daily. 


# 📊 Automação de Relatórios de Vendas e Envio de Indicadores por E-mail

Projeto desenvolvido em **Python** para automatizar a geração de indicadores de desempenho das lojas de uma rede varejista, criar relatórios individuais, gerar rankings de faturamento e enviar e-mails automaticamente para gerentes e diretoria.

---

## 🚀 Funcionalidades

- Importação automática das bases de dados (Excel e CSV);
- Consolidação das informações das lojas;
- Cálculo de indicadores de desempenho:
  - 💰 Faturamento
  - 📦 Diversidade de Produtos
  - 🎫 Ticket Médio
- Comparação automática com metas definidas;
- Geração de relatórios individuais em Excel para cada loja;
- Organização automática dos arquivos em pastas de backup;
- Envio automático de e-mails personalizados para cada gerente;
- Geração do ranking diário e anual de faturamento;
- Envio automático do ranking para a diretoria com os arquivos anexados.

---

# 📂 Estrutura do Projeto

```
Projeto
│
├── Bases de Dados/
│   ├── Vendas.xlsx
│   ├── Lojas.csv
│   └── Emails.xlsx
│
├── Backup Arquivos Lojas/
│   ├── Loja A/
│   ├── Loja B/
│   └── ...
│
├── automacao.py
└── README.md
```

---

# 🛠 Tecnologias Utilizadas

- Python 3
- Pandas
- pathlib
- smtplib
- email.mime
- OpenPyXL (utilizado pelo Pandas para leitura/escrita de arquivos Excel)

---

# 📈 Indicadores Calculados

Para cada loja são calculados:

### Faturamento

- Diário
- Acumulado no período

### Diversidade de Produtos

Quantidade de produtos diferentes vendidos.

### Ticket Médio

Valor médio por venda realizada.

---

# 🎯 Metas

| Indicador | Meta Diária | Meta Anual |
|------------|------------:|-----------:|
| Faturamento | R$ 1.000 | R$ 1.650.000 |
| Diversidade de Produtos | 4 | 120 |
| Ticket Médio | R$ 500 | R$ 500 |

Os resultados são comparados automaticamente às metas utilizando indicadores visuais:

🟢 Meta atingida

🔴 Meta não atingida

---

# 📧 Envio Automático de E-mails

Cada gerente recebe um relatório contendo:

- indicadores do dia;
- indicadores acumulados;
- comparação com as metas;
- planilha da própria loja em anexo.

A diretoria recebe:

- melhor loja do dia;
- pior loja do dia;
- melhor loja do período;
- pior loja do período;
- ranking diário em Excel;
- ranking anual em Excel.

---

# 📊 Ranking Gerado

O sistema cria automaticamente dois arquivos:

- Ranking Diário.xlsx
- Ranking Anual.xlsx

Os rankings são ordenados pelo faturamento das lojas.

---

# ▶️ Como Executar

## 1. Clone o projeto

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

## 2. Instale as dependências

```bash
pip install pandas openpyxl
```

## 3. Organize a estrutura das pastas

```
Bases de Dados/
Backup Arquivos Lojas/
```

## 4. Configure o e-mail

No código substitua:

```python
meu_email = "seu_email@gmail.com"
minha_senha = "sua_senha"
```

> Recomenda-se utilizar uma **Senha de App do Gmail**, evitando armazenar a senha principal da conta.

## 5. Execute

```bash
python automacao.py
```

---

# 📋 Fluxo da Automação

```
Importar Bases
        │
        ▼
Mesclar Dados
        │
        ▼
Separar Vendas por Loja
        │
        ▼
Calcular Indicadores
        │
        ▼
Gerar Relatórios Excel
        │
        ▼
Enviar E-mails aos Gerentes
        │
        ▼
Gerar Rankings
        │
        ▼
Enviar Relatório para Diretoria
```

---

# 🔒 Observações

Por questões de segurança:

- não compartilhe credenciais de e-mail;
- utilize variáveis de ambiente (`.env`) para armazenar senhas;
- adicione arquivos sensíveis ao `.gitignore`.

---

# 💡 Possíveis Melhorias

- Utilização de arquivo `.env` para credenciais;
- Interface gráfica (Tkinter ou Streamlit);
- Agendamento automático com Task Scheduler ou Cron;
- Dashboard em Power BI;
- Logs de execução;
- Tratamento de exceções;
- Envio por Microsoft Outlook (SMTP corporativo);
- Geração de gráficos em PDF.



Projeto desenvolvido para demonstrar automação de processos utilizando Python, manipulação de dados com Pandas e envio automatizado de relatórios por e-mail.
