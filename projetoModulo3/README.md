# Alunos: 
**Guilherme Peres Figueredo |
Juan Henrique de Brito Alves |
Merielly Dos Santos Alves**


# Projeto Módulo 3 – Currículo Gov | Vibecode

## 📌 Desafio Escolhido

**Criação de um gerador de currículos com identidade visual governamental brasileira.**

O projeto visa desenvolver uma aplicação web que permita aos usuários criar e exportar currículos profissionais com design inspirado na identidade visual do governo brasileiro (cores: verde, amarelo e azul). A solução oferece uma experiência de preenchimento intuitiva com preview em tempo real e exportação em PDF.

---

## 🖥️ Protótipo

### Funcionalidades Principais

- ✅ **Formulário interativo** com campos para dados pessoais, experiência, formação e habilidades
- ✅ **Preview em tempo real** – atualizações instantâneas conforme digitação
- ✅ **Design responsivo** – otimizado para diferentes tamanhos de tela
- ✅ **Exportação em PDF** – geração de arquivo A4 pronto para impressão
- ✅ **Identidade visual governamental** – barra colorida (verde, amarelo, azul) e design profissional

### Como Funciona

1. **Entrada de dados**: O usuário preenche as informações na sidebar esquerda (nome, cargo, experiência, etc.)
2. **Visualização ao vivo**: O currículo é atualizado em tempo real na área de preview central
3. **Validação**: Campos têm limite de caracteres e formatos específicos
4. **Exportação**: Ao clicar em "Exportar PDF", a aplicação gera um arquivo profissional

### Tecnologias Utilizadas

- **HTML5** – estrutura e semântica
- **CSS3** – estilos customizados com media queries
- **Tailwind CSS** – framework de utilitários para design responsivo
- **JavaScript** – lógica de atualização de preview e exportação
- **html2pdf.js** – biblioteca para geração de PDFs
- **Google Fonts** – tipografia Inter para visual limpo

---

## ⚙️ Plataforma Utilizada

**Vibecode (HTML + CSS + JavaScript puro)**

### Justificativa da Escolha

- 🎯 **Controle total** – liberdade total sobre design e funcionalidades
- ⚡ **Performance** – aplicação leve e rápida, sem dependências externas complexas
- 💰 **Custo zero** – sem taxas de plataforma ou limites de uso
- 🔧 **Flexibilidade** – fácil customização e integração de bibliotecas
- 📱 **Portabilidade** – funciona em qualquer navegador moderno
- 🎨 **Design personalizado** – implementação exata da identidade visual governamental

---

## 🤖 Ferramentas de IA Utilizadas

### **Gemini Pro**
- 🔍 Geração e refinamento de prompts para estruturação do projeto
- 💡 Ideação de funcionalidades e fluxos de usuário
- 📋 Planejamento da arquitetura da aplicação

### **Google Claude**
- 🚀 Aprimoramento da estrutura do código
- ⚙️ Otimizações de performance e responsividade
- 🔧 Desenvolvimento de funcionalidades complexas (PDF export, validações)

### **GitHub Copilot**
- 📚 Geração de documentação técnica e README
- 📝 Criação de comentários e documentação inline do código
- ✍️ Sugestões de melhorias na estrutura e nomenclatura

---

## ✅ Vantagens Identificadas

1. **Prototipagem Rápida** – Desenvolvimento ágil sem necessidade de backend complexo
2. **Interface Intuitiva** – Usuários com pouco conhecimento técnico conseguem criar currículos profissionais
3. **Integração de Bibliotecas** – Uso de Tailwind e html2pdf sem configurações complexas
4. **Customização Ilimitada** – Código aberto permite ajustes conforme necessário
5. **Acesso Universal** – Funciona online via navegador, sem instalação necessária

---

## ⚠️ Limitações Encontradas

1. **Persistência de Dados** – Sem backend, dados não são salvos automaticamente (usuário perde informações ao recarregar)
2. **Customização de Fontes** – Limitado às fontes disponíveis no Google Fonts
3. **Formatação Avançada** – Dificuldade para formatação texto complexa (negrito, itálico inline no preview)
4. **Compatibilidade de Navegadores** – Algumas funcionalidades podem não funcionar em navegadores antigos
5. **Limite de Conteúdo** – PDFs muito longos podem ter problemas de paginação automática

---

## 📚 Reflexão Crítica

### Como Lidamos com as Limitações

**Problema: Perda de dados ao recarregar**
- ✅ *Solução proposta*: Implementar localStorage para salvar automaticamente dados do formulário

**Problema: Formatação limitada de texto**
- ✅ *Solução criativa*: Uso de espacejamento CSS (pre-line) para preservar quebras de linha e estrutura do texto

**Problema: Paginação em PDFs longos**
- ✅ *Solução criativa*: Aplicação de `page-break-inside: avoid` nas seções CSS para melhor controle de quebras

**Problema: Compatibilidade com navegadores antigos**
- ✅ *Solução proposta*: Testar com polyfills ou considerar transpilação com Babel para produção

---

## 👥 Colaboração

### Responsabilidades e Contribuições

#### 👨‍💻 **Guilherme Peres**
- Definição da estrutura e layout da aplicação
- Integração e refinamento de prompts no Gemini Pro
- Coordenação das funcionalidades principais com o grupo
- Revisão e validação da interface final

#### 👨‍💻 **Juan Henrique**
- Aprimoramentos no Google Claude para otimização do código
- Desenvolvimento de funcionalidades de exportação e validações
- Refinamento da lógica JavaScript e event handlers
- Testes de compatibilidade e performance

#### 👩‍💻 **Merielly Dos Santos**
- Documentação completa com GitHub Copilot
- Criação do README e guias técnicos
- Estruturação de comentários e documentação inline
- Organização da documentação do projeto

### Como Nos Organizamos

- 📌 **Divisão clara de tarefas**: Cada membro focou em sua área específica
- 🔄 **Iterações com IA**: Uso contínuo de ferramentas de IA para aprimoramento
- 📊 **Reuniões de alinhamento**: Sincronização periódica sobre progresso e ajustes
- 🤝 **Revisão colaborativa**: Validação mútua das contribuições finais

---

## 📝 Registro da Aula

| Informação | Detalhes |
|-----------|----------|
| **Data** | 11/05/2026 |
| **Atividade** | Discussão crítica + mini-projeto de aplicação Low Code/No Code |
| **Local** | Laboratório de informática / Quadro branco |
| **Professor(a)** | Kadidja Valéria |
| **Duração** | 4 horas |
| **Resultado** | Protótipo funcional entregue |

---

## 🚀 Próximos Passos

### Melhorias Sugeridas para o Protótipo

- [ ] Implementar **localStorage** para persistência de dados
- [ ] Adicionar **templates de currículo** alternativos
- [ ] Suportar **múltiplos idiomas** (PT-BR, EN, ES)
- [ ] Criar **campo de foto/avatar** com upload
- [ ] Implementar **histórico de versões** de currículos
- [ ] Adicionar **temas personalizáveis** (cores, fontes)
- [ ] Criar **preview de impressão** antes do PDF
- [ ] Adicionar **validação de campos** (email, telefone)

### Evoluções para Projeto Final

- 🔐 **Backend com autenticação** – Usar Node.js/Express para salvar currículos por usuário
- ☁️ **Cloud storage** – Armazenar PDFs em AWS S3 ou Google Cloud
- 🔗 **API REST** – Integrar com serviços de emprego e recrutamento
- 📧 **Envio por email** – Funcionalidade de compartilhamento direto
- 📱 **Aplicativo mobile** – Versão React Native ou Flutter
- 🤖 **IA generativa** – Sugestões automáticas de conteúdo via ChatGPT API
- 📊 **Analytics** – Dashboard de rastreamento de downloads e visualizações

---

## 📄 Licença

Este projeto é parte da disciplina de **Engenharia de Prompts e Aplicações de IA** da faculdade.

---

**✨ Desenvolvido por:** Guilherme Peres, Juan Henrique e Merielly Dos Santos  
**🤖 Com apoio de:** Gemini Pro, Google Claude e GitHub Copilot  
**🎓 Disciplina:** Engenharia de Prompts e Aplicações de IA  
**📅 Semestre:** 2026.1
