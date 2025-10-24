# MD2PDF Converter v2.0

Conversor avançado de Markdown para PDF e DOCX com controles profissionais de formatação em tempo real.

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Características

- ✅ **Editor Markdown** com preview em tempo real lado a lado
- ✅ **14 Fontes profissionais** (Inter, Roboto, Open Sans, Lato, Montserrat, IBM Plex Sans, Playfair Display, Times New Roman, Arial, Century Gothic, Verdana, Georgia, JetBrains Mono, Courier)
- ✅ **Controles avançados de formatação**
  - Seletor de fonte com preview
  - Tamanho de fonte (8pt - 72pt)
  - Peso da fonte (Light, Regular, Medium, Semibold, Bold)
  - Seletor de cor do texto
  - Alinhamento (Esquerda, Centro, Direita, Justificado)
  - Espaçamento de linha (1.0 - 3.0)
  - Estilos rápidos (Negrito, Itálico, Sublinhado)
- ✅ **Exportação profissional**
  - PDF com texto selecionável
  - DOCX (Microsoft Word)
- ✅ **Interface moderna** com design minimalista B&W
- ✅ **Funciona offline** após primeiro carregamento
- ✅ **Responsivo** para diferentes tamanhos de tela

## 📋 Requisitos

### Mínimos
- Navegador moderno (Chrome 90+, Firefox 88+, Edge 90+, Safari 14+)
- JavaScript habilitado
- Conexão internet (primeiro acesso para carregar fontes)

### Recomendados
- Servidor HTTP local (Python ou PowerShell)
- 4GB RAM
- Tela com resolução mínima 1024x768

## 🚀 Instalação

### Windows

```powershell
# 1. Execute o script de setup
.\setup.ps1

# 2. Inicie o servidor
.\server.ps1

# Opcional: use porta diferente
.\server.ps1 -Port 8080
```

### Linux/Mac

```bash
# 1. Torne os scripts executáveis
chmod +x setup.sh server.py

# 2. Execute o setup
./setup.sh

# 3. Inicie o servidor (escolha um)
python3 -m http.server 8000
# ou
./server.py
```

### Instalação Manual

Se preferir não usar os scripts:

```bash
# Python (todos os sistemas)
python -m http.server 8000

# Python 3 (Linux/Mac)
python3 -m http.server 8000

# Node.js (se disponível)
npx serve
```

## 📖 Uso

### 1. Iniciando

1. Abra o navegador em `http://localhost:8000`
2. Digite ou cole seu Markdown no painel esquerdo (Editor)
3. Veja o preview formatado em tempo real no painel direito

### 2. Formatação Básica (Markdown)

```markdown
# Título Principal (H1)
## Subtítulo (H2)
### Seção (H3)

**Texto em negrito**
*Texto em itálico*
~~Texto riscado~~

- Item de lista
- Outro item
  - Sub-item

1. Lista numerada
2. Segundo item

[Link para site](https://exemplo.com)

> Citação importante

`código inline`

```javascript
// Bloco de código
function exemplo() {
  return true;
}
```
```

### 3. Formatação Avançada (Controles)

#### Aplicar formatação em texto específico:

1. **Selecione** o texto no editor que deseja formatar
2. **Configure** as opções na barra de ferramentas:
   - Escolha a fonte
   - Ajuste o tamanho
   - Selecione o peso
   - Escolha a cor
   - Ajuste o espaçamento de linha
3. **Clique** em "Aplicar Formatação"

O texto selecionado será envolvido com tags HTML inline com os estilos escolhidos.

#### Botões de alinhamento rápido:

- **←** Alinhar à esquerda
- **⋮** Centralizar
- **→** Alinhar à direita
- **≡** Justificar

#### Botões de estilo rápido:

- **B** Negrito (`**texto**`)
- **I** Itálico (`*texto*`)
- **U** Sublinhado (`<u>texto</u>`)

### 4. Exportação

#### PDF

1. Digite o nome do arquivo no campo "nome do arquivo"
2. Clique no botão **PDF**
3. Na janela de impressão:
   - Selecione "Salvar como PDF"
   - Escolha o local de destino
   - Clique em "Salvar"

O PDF gerado terá:
- Texto selecionável e pesquisável
- Formatação preservada
- Fontes incorporadas
- Tamanho A4
- Margens de 2.5cm

#### DOCX (Microsoft Word)

1. Digite o nome do arquivo no campo "nome do arquivo"
2. Clique no botão **DOCX**
3. O arquivo será baixado automaticamente

O DOCX gerado inclui:
- Estrutura de títulos (H1, H2, H3)
- Parágrafos formatados
- Listas
- Formatação básica (negrito, itálico)

## 🎨 Fontes Disponíveis

### Sans-serif (sem serifa)
- **Inter** - Design moderno e legível
- **Roboto** - Geometria equilibrada
- **Open Sans** - Humanista e amigável
- **Lato** - Elegante e versátil
- **Montserrat** - Geométrica urbana
- **IBM Plex Sans** - Corporativa moderna
- **Arial** - Clássica universal
- **Century Gothic** - Geométrica clean
- **Verdana** - Otimizada para telas

### Serif (com serifa)
- **Playfair Display** - Elegante e dramática
- **Times New Roman** - Tradicional acadêmica
- **Georgia** - Otimizada para telas

### Monospace (código)
- **JetBrains Mono** - Desenvolvida para programação
- **Courier** - Clássica de máquina de escrever

## 📁 Estrutura do Projeto

```
md2pdf-converter/
│
├── index.html          # Aplicação principal (28KB)
├── setup.ps1           # Setup para Windows
├── setup.sh            # Setup para Linux/Mac
├── server.ps1          # Servidor HTTP Windows
├── server.py           # Servidor HTTP multiplataforma
├── README.md           # Esta documentação
│
├── lib/                # Bibliotecas locais (opcional)
│   ├── marked.min.js
│   ├── docx.min.js
│   └── FileSaver.min.js
│
├── assets/             # Assets do projeto
└── docs/               # Documentação adicional
```

## 🔧 Tecnologias Utilizadas

### Frontend
- **HTML5/CSS3** - Estrutura e estilo
- **JavaScript ES6+** - Lógica da aplicação
- **CSS Grid & Flexbox** - Layout responsivo

### Bibliotecas (CDN)
- **Marked.js 9.1.6** - Parsing Markdown → HTML
- **docx.js 7.8.2** - Geração de arquivos DOCX
- **FileSaver.js 2.0.5** - Download de arquivos no navegador

### Fontes (Google Fonts)
- Inter, Roboto, Open Sans, Lato, Montserrat
- IBM Plex Sans, Playfair Display
- JetBrains Mono

### APIs Nativas
- **Window.print()** - Geração de PDF
- **File API** - Manipulação de arquivos
- **Selection API** - Seleção de texto

## ⚙️ Configurações Avançadas

### Usar bibliotecas locais (offline completo)

1. Execute `setup.ps1` ou `setup.sh` para baixar bibliotecas
2. Edite `index.html` e substitua as URLs CDN:

```html
<!-- Antes -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/marked/9.1.6/marked.min.js"></script>

<!-- Depois -->
<script src="lib/marked.min.js"></script>
```

### Personalizar porta do servidor

```bash
# Python
python -m http.server 3000

# PowerShell
.\server.ps1 -Port 3000

# Edite server.py
PORT = 3000  # Linha 12
```

### Adicionar novas fontes

1. Adicione a fonte no Google Fonts (linha 12 do index.html)
2. Adicione opção no select (linha 409-424):

```html
<option value="'Sua Fonte', sans-serif">Sua Fonte</option>
```

## 🐛 Troubleshooting

### PDF não gera

**Problema:** Clico em PDF mas nada acontece

**Soluções:**
- Verifique se há conteúdo no editor
- Permita pop-ups no navegador
- Tente outro navegador (Chrome recomendado)
- Verifique console do navegador (F12) por erros

### DOCX não baixa

**Problema:** Erro ao gerar DOCX

**Soluções:**
- Verifique conexão com internet (primeira vez)
- Aguarde carregamento completo da página
- Verifique se `docx.js` foi carregado (console F12)
- Tente formatar o Markdown de forma mais simples

### Fontes não aparecem

**Problema:** Todas as fontes parecem iguais

**Soluções:**
- Verifique conexão com internet (Google Fonts)
- Limpe cache do navegador (Ctrl+Shift+Del)
- Verifique se Google Fonts não está bloqueado
- Aguarde alguns segundos após carregar a página

### Servidor não inicia (Windows)

**Problema:** Erro ao executar `server.ps1`

**Soluções:**
```powershell
# Permitir execução de scripts
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

# Verificar se porta está em uso
netstat -ano | findstr :8000

# Usar porta alternativa
.\server.ps1 -Port 8080
```

### Servidor não inicia (Linux/Mac)

**Problema:** `Permission denied` ou porta em uso

**Soluções:**
```bash
# Tornar executável
chmod +x server.py

# Verificar porta
lsof -i :8000

# Matar processo na porta
kill -9 $(lsof -ti:8000)

# Usar porta alternativa
python3 -m http.server 8080
```

### Preview não atualiza

**Problema:** Digito mas preview não muda

**Soluções:**
- Recarregue a página (F5)
- Limpe cache (Ctrl+Shift+R)
- Verifique console por erros JavaScript
- Certifique-se que `marked.js` foi carregado

## 💡 Dicas e Truques

### Workflow Eficiente

1. **Escreva primeiro** todo o conteúdo em Markdown
2. **Revise** o preview geral
3. **Selecione e formate** seções específicas
4. **Exporte** quando finalizar

### Formatação Consistente

- Use a mesma fonte para todo o documento
- Limite-se a 2-3 tamanhos de fonte
- Use espaçamento de linha 1.5-1.6 para legibilidade
- Prefira alinhamento justificado para documentos formais

### Atalhos Úteis

- **Ctrl+A** no editor: seleciona todo o texto
- **Ctrl+F** no navegador: busca no preview
- **F11**: modo tela cheia
- **Ctrl+P**: imprimir/salvar PDF direto

### Boas Práticas

- Salve o Markdown em arquivo `.md` local
- Use nomes descritivos para arquivos exportados
- Teste o PDF antes de compartilhar
- Mantenha backup do Markdown original

## 📊 Limitações Conhecidas

- DOCX preserva formatação básica (não inclui estilos HTML inline avançados)
- Fontes do PDF dependem do sistema para impressão
- Tabelas complexas podem ter layout diferente no DOCX
- Imagens devem estar em URL pública para aparecer no PDF
- Tamanho máximo recomendado: 50 páginas

## 🔐 Privacidade e Segurança

- **100% Client-side**: Todo processamento ocorre no navegador
- **Sem upload**: Nenhum dado é enviado para servidores externos
- **Sem tracking**: Não há analytics ou cookies
- **Offline**: Funciona sem internet após primeiro carregamento
- **Open Source**: Código auditável

## 📄 Licença

Este projeto é disponibilizado como software livre para uso pessoal e comercial.

## 🤝 Contribuições

Sugestões e melhorias são bem-vindas!

## 📞 Suporte

Para problemas ou dúvidas:
1. Consulte a seção **Troubleshooting**
2. Verifique o console do navegador (F12)
3. Abra uma issue no repositório do projeto

## 🎯 Casos de Uso

- **Documentação técnica** com código e formatação precisa
- **Artigos e posts** com formatação personalizada
- **Relatórios profissionais** em PDF ou Word
- **Anotações acadêmicas** com estrutura clara
- **Especificações de projeto** exportáveis
- **Manuais e guias** com múltiplas seções

## 🚧 Roadmap

Funcionalidades planejadas:
- [ ] Temas de cores (claro/escuro)
- [ ] Templates prontos
- [ ] Suporte a tabelas avançadas no DOCX
- [ ] Exportação para HTML standalone
- [ ] Atalhos de teclado personalizáveis
- [ ] Histórico de formatação
- [ ] Salvar/carregar configurações

---

**MD2PDF Converter v2.0** - Desenvolvido com foco em simplicidade e eficiência.

*Última atualização: 2024*
