# 📄 Conversor Markdown para PDF (Local)

Este projeto contém um conversor de Markdown para PDF que utiliza `html2canvas` para renderização fiel do preview. A aplicação foi desenvolvida para documentação técnica de endpoints de pagamento e sistemas financeiros.

## 🚀 Como Executar o Projeto

Para evitar o erro de segurança **"Tainted canvases may not be exported"** (causado ao abrir arquivos HTML diretamente com o protocolo `file:///`), é necessário executar a aplicação em um servidor web local.

O projeto já está configurado para usar o `live-server` com um único comando `npm start`.

### Pré-requisitos

Certifique-se de ter o **Node.js** (versão 14 ou superior) e o **npm** (versão 6 ou superior) instalados na sua máquina.

### Passos de Execução

1. **Instale as dependências** do projeto:
   ```bash
   npm install
   ```

2. **Inicie o servidor local** e abra o navegador automaticamente:
   ```bash
   npm start
   ```

O servidor será iniciado em `http://localhost:8080` e você poderá acessar a aplicação, permitindo a correta geração do PDF.

## 🛠️ Funcionalidades

- **Editor Markdown**: Interface de edição com syntax highlighting
- **Preview em Tempo Real**: Visualização instantânea do conteúdo Markdown
- **Geração de PDF**: Conversão do preview para PDF usando html2canvas
- **Exemplo Pronto**: Documentação técnica de endpoint de duplicação de cartão
- **Design Responsivo**: Interface adaptável para diferentes tamanhos de tela

## 📋 Tecnologias Utilizadas

- **HTML5/CSS3**: Interface e estilização
- **JavaScript Vanilla**: Lógica da aplicação
- **Marked.js**: Parser de Markdown
- **html2canvas**: Captura de tela para PDF
- **jsPDF**: Geração de arquivos PDF
- **live-server**: Servidor de desenvolvimento local

## 🔧 Configuração Técnica

### html2canvas Configuration

A aplicação está configurada para lidar com recursos externos e CORS:

```javascript
html2canvas(content, {
    scale: 2,
    useCORS: true,
    logging: false,
    backgroundColor: '#ffffff'
});
```

### Estrutura do Projeto

```
md.to.pdf.generator/
├── index.html              # Aplicação principal
├── package.json            # Configurações do projeto
├── README.md              # Documentação
└── fluxograma_duplicate_card.png  # Imagem de exemplo
```

## 🚨 Solução de Problemas

### Erro "Tainted Canvas"

Se você encontrar o erro "Tainted canvases may not be exported", certifique-se de que:

1. A aplicação está rodando em um servidor HTTP (não file://)
2. O `live-server` está sendo usado
3. A configuração `useCORS: true` está ativa

### Problemas de Performance

Para documentos muito grandes:

- Ajuste o `scale` no html2canvas (valores menores = mais rápido)
- Considere dividir o conteúdo em seções menores
- Use `logging: false` para reduzir overhead

## 📝 Uso da Aplicação

1. **Editar**: Digite ou cole seu conteúdo Markdown no editor à esquerda
2. **Visualizar**: Veja o preview em tempo real à direita
3. **Gerar PDF**: Clique em "⬇️ Gerar PDF" para baixar o arquivo
4. **Exemplo**: Use "📝 Carregar Exemplo" para ver a documentação técnica

## 🎯 Casos de Uso

Esta ferramenta é ideal para:

- Documentação técnica de APIs
- Relatórios de sistemas financeiros
- Documentação de endpoints de pagamento
- Manuais de integração
- Especificações técnicas

## 📄 Exemplo Incluído

O projeto inclui um exemplo completo de documentação técnica para o endpoint `/cards/duplicate-card`, demonstrando:

- Especificações de API
- Fluxos de validação
- Códigos de erro
- Estrutura de dados
- Considerações de segurança

## 🔒 Segurança

- A aplicação roda localmente, sem envio de dados para servidores externos
- Dados sensíveis permanecem no ambiente local
- Não há coleta de informações pessoais

## 📞 Suporte

Para problemas ou dúvidas sobre a aplicação, verifique:

1. Se o Node.js está instalado corretamente
2. Se as dependências foram instaladas (`npm install`)
3. Se o servidor está rodando em HTTP (não file://)
4. Console do navegador para erros específicos
