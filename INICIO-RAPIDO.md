# 🚀 INÍCIO RÁPIDO - MD2PDF Converter

Este repositório contém um **Conversor de Markdown para PDF/DOCX** com interface web moderna.

## ⚠️ IMPORTANTE

- **NÃO abra** o arquivo `index.html` diretamente no navegador (duplo clique)
- **SEMPRE use** um servidor HTTP local
- O arquivo precisa ser servido via HTTP para funcionar corretamente

## 📍 O que tem neste repositório?

- `index.html` - Editor e Conversor MD2PDF (interface web completa)
- `server.py` - Servidor HTTP para Linux/Mac
- `server.ps1` - Servidor HTTP para Windows
- `setup.sh` - Script de configuração Linux/Mac
- `setup.ps1` - Script de configuração Windows

## 🎯 Como usar (WINDOWS - Recomendado)

### Passo 1: Abra o PowerShell no diretório do projeto

```powershell
# Navegue até a pasta do projeto
cd D:\MARKDOWN-CONVERTER-main\MARKDOWN-CONVERTER-main
```

### Passo 2: Execute o servidor

```powershell
# Opção A: Porta padrão 8000
.\server.ps1

# Opção B: Porta personalizada 8080
.\server.ps1 -Port 8080
```

### Passo 3: Abra o navegador

Acesse: **http://localhost:8000** (ou a porta que você escolheu)

## 🐧 Como usar (LINUX/MAC)

```bash
# Navegue até a pasta do projeto
cd /caminho/para/MARKDOWN-CONVERTER

# Torne o servidor executável
chmod +x server.py

# Execute o servidor
./server.py

# Ou use Python diretamente
python3 -m http.server 8000
```

Acesse: **http://localhost:8000**

## ❓ Problemas Comuns

### ❌ "Não consigo acessar" ou "Página não carrega"

**Causa:** Você tentou abrir o `index.html` diretamente (file://)

**Solução:**
1. Feche o arquivo
2. Execute o servidor (ver passos acima)
3. Acesse via http://localhost:8000

### ❌ "Porta já em uso"

**Solução Windows:**
```powershell
# Use porta diferente
.\server.ps1 -Port 8080
```

**Solução Linux/Mac:**
```bash
python3 -m http.server 8080
```

### ❌ "Erro ao ler arquivo" (Windows PowerShell)

**Causa:** Bug corrigido na versão atual do server.ps1

**Solução:**
1. Certifique-se de estar na pasta correta
2. Execute o comando `pwd` ou `cd` para verificar
3. Use a versão corrigida do server.ps1 deste commit

### ❌ "Fontes não aparecem" ou "Estilo quebrado"

**Causa:** Abriu o arquivo diretamente sem servidor

**Solução:** Use o servidor HTTP (as fontes vêm do Google Fonts via internet)

## ✅ Checklist de Verificação

Antes de reportar problemas, verifique:

- [ ] Estou executando via servidor HTTP (não file://)
- [ ] O servidor está rodando sem erros
- [ ] Estou acessando http://localhost:PORTA
- [ ] Tenho conexão com internet (para fontes Google)
- [ ] O navegador está atualizado (Chrome, Firefox, Edge)

## 🎨 O que é o MD2PDF Converter?

É um editor de Markdown com preview em tempo real que permite:

- ✅ Escrever em Markdown
- ✅ Ver preview formatado ao vivo
- ✅ Escolher fontes (14 opções)
- ✅ Personalizar formatação (tamanho, cor, peso)
- ✅ Exportar para PDF
- ✅ Exportar para DOCX (Word)

## 📖 Uso Básico

1. **Digite** seu texto em Markdown no painel esquerdo
2. **Veja** o preview formatado no painel direito
3. **Personalize** usando os controles superiores
4. **Exporte** clicando em PDF ou DOCX

## 📚 Mais Informações

Consulte o **README.md** completo para:
- Sintaxe Markdown detalhada
- Todas as funcionalidades
- Troubleshooting avançado
- Dicas e truques

## 🔗 Links Úteis

- Acesso local: http://localhost:8000
- Porta alternativa: http://localhost:8080
- Documentação completa: [README.md](README.md)

---

**Dúvidas?** Leia o README.md ou verifique o console do navegador (F12) para erros.
