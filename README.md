# 💼 NETCURSOS – Painel Financeiro

> Sistema de gestão financeira integrado ao portal de alunos da plataforma **NETCURSOS**.  
> Desenvolvido em PHP com MySQL e Bootstrap, o painel permite administrar cobranças, recebimentos, despesas e visualizar o **DRE (Demonstrativo de Resultados do Exercício)** de forma simples e eficiente.

---

## 🚀 Funcionalidades Principais

### 🔹 Financeiro
- **Gerar Cobranças:** criação de boletos e QR Codes Pix para alunos.  
- **Baixa de Pagamentos:** registrar recebimentos e atualizar status de pagamentos.  
- **Contas a Receber:** acompanhamento geral de receitas e inadimplência.  
- **Contas a Pagar:** gestão de despesas e fornecedores com controle de vencimentos.  
- **DRE:** relatório mensal e **dashboard anual** com receitas, despesas e lucro/prejuízo.

### 🔹 Recursos Extras
- Filtros por mês/ano.
- Gráfico anual interativo com **Chart.js**.
- Cadastro, edição e exclusão de despesas.
- Interface responsiva e moderna com **Bootstrap 5**.
- Relatórios otimizados para exportação (PDF opcional).

---

## 🧱 Estrutura de Diretórios


---

## 🗃️ Estrutura de Banco de Dados

### 🧾 `recebimentos`
Armazena todos os pagamentos recebidos dos alunos.

| Campo | Tipo | Descrição |
|-------|------|------------|
| id | int | Identificador |
| contrato_id | int | Relacionamento com o contrato do aluno |
| data_pagamento | date | Data de pagamento |
| valor_pago | decimal(10,2) | Valor recebido |
| forma_pagamento | varchar(20) | Pix, boleto, etc. |
| mes_referencia | varchar(7) | Mês de referência |
| comprovante | varchar(255) | Nome do arquivo |
| status | varchar(20) | pago / pendente |

### 💸 `contas_pagar`
Controle de despesas e contas a pagar.

| Campo | Tipo | Descrição |
|-------|------|------------|
| id | int | Identificador |
| descricao | varchar(255) | Descrição da despesa |
| valor | decimal(10,2) | Valor da despesa |
| data_vencimento | date | Data de vencimento |
| status | enum('Pendente','Pago') | Situação atual |
| observacoes | text | Campo livre |
| data_cadastro | timestamp | Criação automática |

---

## ⚙️ Instalação e Configuração

### 🔧 Requisitos
- PHP **7.4+**
- MySQL **5.7+**
- Servidor Apache ou Nginx
- Extensão `mysqli` habilitada


