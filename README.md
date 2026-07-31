# 🦷 Relatório Executivo - Menezes & Modenesi Odontologia

[![GitHub](https://img.shields.io/badge/GitHub-Clinica-blue)](https://github.com)
[![Status](https://img.shields.io/badge/Status-Ativo-green)]()
[![Versão](https://img.shields.io/badge/Versão-5.0-orange)]()

**Sistema web completo de gestão financeira e administrativo para clínicas odontológicas**, com sincronização automática de dados e integração com Firebase.

## ✨ Destaques

### 🔗 Sinergia de Cadastros (Nova!)
- **Cadastros conectados**: Dentistas e Fornecedores aparecem automaticamente nos formulários de Entradas e Saídas
- **Sem digitação repetida**: Selecione direto da lista de cadastros
- **Sincronização em tempo real**: Adicione um cadastro e ele já está disponível em todas as abas

### 💾 Persistência de Dados
- **localStorage**: Armazena todos os dados localmente
- **Firebase Real-time**: Sincroniza backups automáticos com Firebase
- **Exportação**: Exporte dados em CSV para Excel/Planilhas

### 📊 Dashboard Interativo
- Estatísticas do mês (Entradas, Saídas, Saldo)
- Gráficos de formas de pagamento e tipos de despesa
- Fluxo de caixa visual

## 🚀 Funcionalidades

### 📥 Entradas
- Registro de recebimentos de pacientes
- Associação automática com dentista
- Múltiplas formas de pagamento
- Histórico completo com filtro de busca
- Exportação para CSV

### 📤 Saídas
- Controle de despesas e pagamentos
- Categorização por tipo
- Seleção automática de fornecedores
- Status de pagamento (Pago/Provisório)
- Data de vencimento e acompanhamento

### 👨‍⚕️ Cadastro de Dentistas
- Registro de profissionais
- CRO (Conselho Regional)
- Especialidades
- Contato (Email, Telefone)
- **Sincronização automática com campo de Dentista em Entradas**

### 🏢 Cadastro de Fornecedores
- Razão Social e CNPJ
- Endereço e Cidade
- Contato e Email
- **Sincronização automática com campo de Fornecedor em Saídas**

### 📋 Tipos de Despesas
- Categorização customizável
- Código de identificação
- Descrição detalhada

### ⚙️ Configurações
- Dados da clínica
- Alteração de senha
- Upload de logo customizado
- Backup/Restauração de dados

### 📈 Relatórios
- Análise de entradas por forma de pagamento
- Distribuição de saídas por tipo
- Fluxo de caixa mensal

## 🛠️ Tecnologias

- **Frontend**: HTML5, CSS3, JavaScript vanilla
- **Dados**: localStorage + Firebase Realtime Database
- **Gráficos**: Chart.js 3.9.1
- **Exportação**: XLSX, html2pdf.js
- **Responsividade**: Mobile-first design

## 📋 Requisitos

- Navegador moderno com suporte a ES6
- Conexão com internet (para Firebase)
- JavaScript ativado

## 🚀 Como Começar

### 1. Instalação

Clone o repositório e abra o arquivo HTML no seu navegador:

```bash
git clone https://github.com/seu-usuario/clinica.git
cd clinica
# Abra o arquivo em seu navegador
open relatorio_executivo_v5_SINERGIA_COMPLETA.html
```

Ou acesse diretamente no navegador (sem instalação necessária).

### 2. Primeiro Acesso

**Credenciais padrão:**
- Usuário: `user@demo.com`
- Senha: `123456`

### 3. Primeiros Passos

#### Passo 1: Configure a Clínica
1. Vá para **⚙️ Configurações**
2. Preencha os dados: Nome, CNPJ, Email, Telefone
3. Faça upload de sua logo (opcional)
4. Clique em **✅ Salvar Configuração**

#### Passo 2: Cadastre Dentistas
1. Vá para **👨‍⚕️ Dentistas**
2. Preencha: Nome, CRO, Email, Telefone, Especialidade
3. Clique em **✅ Adicionar Dentista**
4. ✨ *O dentista aparecerá automaticamente no campo de Entradas*

#### Passo 3: Cadastre Fornecedores
1. Vá para **🏢 Fornecedores**
2. Preencha: Razão Social, CNPJ, Email, Telefone, Endereço
3. Clique em **✅ Adicionar Fornecedor**
4. ✨ *O fornecedor aparecerá automaticamente no campo de Saídas*

#### Passo 4: Registre Entradas (Receitas)
1. Vá para **💰 Entradas**
2. Preencha os dados:
   - Data do atendimento
   - Nome do paciente
   - **Selecione o Dentista** (lista populada automaticamente)
   - Valor cobrado
   - Forma de pagamento
3. Clique em **✅ Adicionar Entrada**

#### Passo 5: Registre Saídas (Despesas)
1. Vá para **📤 Saídas**
2. Preencha os dados:
   - Data da despesa
   - Tipo (Salário, Aluguel, Material, etc.)
   - **Selecione o Fornecedor** (lista populada automaticamente)
   - Valor
   - Forma de pagamento
   - Status (Pago/Provisório)
3. Clique em **✅ Adicionar Saída**

#### Passo 6: Visualize o Dashboard
1. Vá para **📊 Dashboard**
2. Acompanhe:
   - Total de Entradas do mês
   - Total de Saídas do mês
   - Saldo (Positivo/Negativo)
   - Gráficos de distribuição

## 🔄 Sincronização Automática (SINERGIA)

### Como Funciona

```
CADASTRO → BANCO DE DADOS LOCAL → SELECT AUTOMÁTICO

1. Você cadastra um Dentista
   ↓
2. Sistema salva em localStorage
   ↓
3. Select de "Dentista" em Entradas é atualizado
   ↓
4. Próxima entrada: selecione direto da lista
```

### Exemplo Prático

**Sem Sinergia (antes):**
1. Cadastra Dr. João - salva em Dentistas
2. Vai para Entradas
3. Digita "Dr. João" manualmente no campo de Dentista

**Com Sinergia (agora):**
1. Cadastra Dr. João - salva em Dentistas
2. Vai para Entradas
3. Seleciona "Dr. João" do dropdown
4. Sem erros de digitação! ✨

## 💾 Backup e Restauração

### Fazer Backup
1. Vá para **⚙️ Configurações**
2. Clique em **💾 Fazer Backup**
3. Arquivo JSON será baixado automaticamente

### Restaurar Backup
1. Vá para **⚙️ Configurações**
2. Clique em **📂 Restaurar**
3. Selecione o arquivo `.json` de backup
4. Dados serão restaurados automaticamente

## 🔐 Firebase Integração

### Configuração
O Firebase já vem configurado para a clínica Menezes & Modenesi:
- **Projeto**: clinica2-8f789
- **Database**: Firebase Realtime Database

### Como Usar

#### Salvar no Firebase
1. Clique no botão **💾 Salvar** (canto superior direito)
2. Verifique o status:
   - 🟢 **Conectado**: Dados sincronizados
   - 🔴 **Desconectado**: Tente reconectar

#### Testar Conexão
1. Clique em **🧪 Testar**
2. Sistema verificará a conexão com Firebase

### O que é Sincronizado?
- ✅ Todas as Entradas
- ✅ Todas as Saídas
- ✅ Cadastro de Dentistas
- ✅ Cadastro de Fornecedores
- ✅ Configurações da clínica

## 📊 Relatórios e Análises

### Dashboard
- **Estatísticas**: Total Entradas, Saídas, Saldo e Transações
- **Gráficos**: Formas de pagamento, Tipos de despesa

### Exportação
Todos os dados podem ser exportados em formato CSV:
- 📥 Entradas → Excel
- 📥 Saídas → Excel
- 📥 Dentistas → Excel
- 📥 Fornecedores → Excel
- 📥 Tipos de Despesas → Excel

## 🔒 Segurança

### Autenticação
- Senha armazenada com encode básico
- Altere a senha em **⚙️ Configurações**
- Padrão: `123456`

### Dados
- Armazenados localmente (localStorage)
- Backup encriptado no Firebase
- Backup/Restauração manual disponível

### Boas Práticas
1. Altere a senha padrão
2. Faça backups regularmente
3. Guarde o arquivo de backup em local seguro

## 📱 Responsividade

O sistema funciona em:
- 💻 Desktop (1920px+)
- 💻 Laptop (1024px+)
- 📱 Tablet (768px+)
- 📱 Mobile (320px+)

## 🐛 Solução de Problemas

### "Os selects de Dentista/Fornecedor estão vazios"
**Solução**: Você precisa cadastrar Dentistas e Fornecedores primeiro na aba respectiva

### "Dados não salvam"
**Solução**: 
1. Verifique se localStorage está ativado no navegador
2. Tente limpar cache do navegador
3. Reinstale a página

### "Firebase não conecta"
**Solução**:
1. Verifique conexão com internet
2. Clique em **🧪 Testar** para diagnóstico
3. Tente novamente em alguns minutos

### "Perdi meus dados"
**Solução**: 
1. Recupere de um backup anterior
2. Vá para **⚙️ Configurações**
3. Clique em **📂 Restaurar** e selecione o arquivo

## 📈 Roadmap (Futuro)

- [ ] Autenticação com Google/Facebook
- [ ] Dark Mode
- [ ] Sincronização automática com WhatsApp
- [ ] Integração com sistemas de pagamento
- [ ] App mobile nativa
- [ ] Relatórios avançados com PDF
- [ ] Agendamento de pacientes
- [ ] Prontuário eletrônico

## 📞 Suporte

Para dúvidas ou sugestões:
- 📧 Email: contato@clinica.com
- 📱 WhatsApp: Configurável em Configurações

## 📄 Licença

Este projeto é de uso exclusivo da Clínica Menezes & Modenesi Odontologia.

## 👨‍💻 Desenvolvido por

**Wagner** - Especialista em Sistemas Web para Clínicas Odontológicas

---

## 🎯 Versão Atual

**v5.0 - SINERGIA COMPLETA**
- ✨ Sincronização automática de Dentistas com Entradas
- ✨ Sincronização automática de Fornecedores com Saídas
- 🔄 Atualização automática de selects
- 📦 localStorage + Firebase integrado
- 💾 Backup e restauração completa

---

<div align="center">

**⭐ Se este projeto foi útil, considere dar uma estrela no GitHub! ⭐**

Made with 💜 for Menezes & Modenesi Odontologia

</div>
