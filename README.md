# 📄 Conversor Markdown para PDF

Um conversor completo e moderno de Markdown para PDF com interface intuitiva, preview em tempo real e links clicáveis. Desenvolvido para documentação técnica, relatórios e qualquer conteúdo que precise ser convertido de Markdown para PDF de forma profissional.

## ✨ Funcionalidades

### 🎯 Principais Recursos
- **Editor Markdown Intuitivo**: Interface de edição com syntax highlighting
- **Preview em Tempo Real**: Visualização instantânea do conteúdo Markdown
- **Geração de PDF Completa**: Conversão do preview para PDF sem cortes de conteúdo
- **Links Clicáveis**: Links funcionais no PDF gerado
- **Upload de Arquivos**: Suporte a drag & drop para arquivos .md
- **Quebra de Páginas Inteligente**: Evita quebras inadequadas em elementos importantes
- **Layout Responsivo**: Interface adaptável para diferentes tamanhos de tela
- **Suporte a Imagens**: Imagens locais e externas
- **Estilização Completa**: Suporte a todos os elementos Markdown

### 🔗 Links Clicáveis no PDF
- Links do Markdown são convertidos em links clicáveis no PDF
- Funcionam em qualquer visualizador de PDF
- Abrem automaticamente no navegador padrão

### 📱 Interface Responsiva
- Design moderno e limpo
- Adaptável para desktop, tablet e mobile
- Controles intuitivos e acessíveis

## 🚀 Como Executar

### Pré-requisitos
- **Node.js** (versão 14 ou superior)
- **npm** (versão 6 ou superior)

### Instalação e Execução

1. **Clone o repositório**:
   ```bash
   git clone <url-do-repositorio>
   cd md.to.pdf.generator
   ```

2. **Instale as dependências**:
   ```bash
   npm install
   ```

3. **Inicie o servidor local**:
   ```bash
   npm start
   ```

4. **Acesse a aplicação**:
   - O navegador abrirá automaticamente em `http://localhost:8080`
   - Ou acesse manualmente a URL

## 📖 Como Usar

### 1. **Editar Conteúdo**
- Digite ou cole seu conteúdo Markdown no editor à esquerda
- Use o exemplo padrão como referência clicando em "📝 Exemplo Padrão"

### 2. **Visualizar Preview**
- Veja o preview em tempo real no painel à direita
- O preview mostra exatamente como ficará o PDF

### 3. **Upload de Arquivos**
- Clique em "📁 Upload .md" para carregar arquivos
- Ou arraste e solte arquivos .md diretamente no editor
- Suporta arquivos .md, .markdown e .txt

### 4. **Gerar PDF**
- Clique em "⬇️ Gerar PDF" para baixar o arquivo
- O PDF será gerado com todo o conteúdo e links clicáveis
- Nome do arquivo baseado no título do documento

## 🛠️ Tecnologias Utilizadas

### Frontend
- **HTML5/CSS3**: Interface e estilização responsiva
- **JavaScript Vanilla**: Lógica da aplicação
- **Marked.js**: Parser de Markdown
- **html2canvas**: Captura de tela para PDF
- **jsPDF**: Geração de arquivos PDF

### Desenvolvimento
- **live-server**: Servidor de desenvolvimento local
- **Node.js/npm**: Gerenciamento de dependências

## 📁 Estrutura do Projeto

```
md.to.pdf.generator/
├── index.html              # Aplicação principal
├── package.json            # Configurações do projeto
├── package-lock.json       # Lock file das dependências
├── README.md              # Documentação
├── images/                # Imagens de exemplo
│   └── example-image.png
└── .gitignore             # Arquivo de exclusões do Git
```

## ⚙️ Configurações Técnicas

### html2canvas Configuration
```javascript
html2canvas(container, {
    scale: 2,                    // Qualidade da imagem
    useCORS: true,              // Suporte a recursos externos
    allowTaint: true,           // Permite imagens externas
    backgroundColor: '#ffffff',  // Fundo branco
    logging: false              // Desabilita logs
});
```

### jsPDF Configuration
```javascript
const pdf = new jsPDF({
    orientation: 'portrait',    // Orientação vertical
    unit: 'mm',                // Unidade em milímetros
    format: 'a4'               // Formato A4
});
```

## 🎨 Elementos Markdown Suportados

### Texto
- **Negrito** e *itálico*
- `Código inline`
- ~~Riscado~~
- Links [texto](url)

### Cabeçalhos
- # H1
- ## H2
- ### H3
- #### H4

### Listas
- Listas não ordenadas
- 1. Listas ordenadas
- [ ] Listas de tarefas

### Código
- Blocos de código com syntax highlighting
- Código inline

### Outros
- > Citações
- Tabelas
- Imagens
- Linhas horizontais
- Links clicáveis

## 🚨 Solução de Problemas

### Erro "Tainted Canvas"
Se encontrar o erro "Tainted canvases may not be exported":
1. Certifique-se de que a aplicação está rodando em servidor HTTP
2. Use `npm start` para iniciar o live-server
3. Não abra o arquivo diretamente no navegador (file://)

### Problemas de Performance
Para documentos muito grandes:
- Ajuste o `scale` no html2canvas (valores menores = mais rápido)
- Considere dividir o conteúdo em seções menores
- Use `logging: false` para reduzir overhead

### Links Não Funcionam
- Verifique se os links estão no formato correto: `[texto](url)`
- Links relativos podem não funcionar no PDF
- Use URLs completas (https://) para melhor compatibilidade

## 🎯 Casos de Uso

Esta ferramenta é ideal para:

- **Documentação Técnica**: APIs, endpoints, integrações
- **Relatórios**: Relatórios técnicos e de negócios
- **Manuais**: Manuais de usuário e técnicos
- **Especificações**: Especificações de sistemas
- **Documentação de Código**: READMEs e documentação de projetos
- **Apresentações**: Conteúdo para apresentações
- **Artigos**: Artigos técnicos e tutoriais

## 🔒 Segurança e Privacidade

- **100% Local**: A aplicação roda completamente no seu computador
- **Sem Dados Externos**: Nenhum conteúdo é enviado para servidores externos
- **Privacidade Total**: Seus dados permanecem no ambiente local
- **Sem Tracking**: Não há coleta de informações pessoais

## 📄 Exemplo Incluído

O projeto inclui um exemplo completo demonstrando:
- Títulos e subtítulos
- Parágrafos de texto
- Listas ordenadas e não ordenadas
- Blocos de código
- Tabelas
- Citações
- Links clicáveis
- Imagens

## 🤝 Contribuição

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📞 Suporte

Para problemas ou dúvidas:

1. Verifique se o Node.js está instalado corretamente
2. Confirme se as dependências foram instaladas (`npm install`)
3. Certifique-se de que o servidor está rodando em HTTP
4. Verifique o console do navegador para erros específicos
5. Abra uma issue no repositório

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
