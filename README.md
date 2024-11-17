# Trabalho Final de Disciplina: Navegador com Simulação de HTML

## 📅 Data de Entrega

**06/12/2024, até as 19:30h.**  
- O trabalho poderá ser realizado em **grupos de até 3 alunos**.  
- A entrega deve ser feita no formato `.zip` pelo Moodle.  
- **Atrasos não serão aceitos.**

---

## 🛠️ Objetivo do Projeto

Expandir o código fornecido para criar um **simulador de navegador** que permita:  
1. **Criação de novas abas.**  
2. **Remoção de abas existentes.**  
3. **Leitura e exibição de conteúdo HTML simulado** em abas.  

O projeto utiliza **C++ orientado a objetos**, **leitura de arquivos** e a biblioteca **SFML** para interface gráfica.

---

## 🔍 Requisitos Funcionais

### 1. **Criação de Novas Abas**
- Adicione um botão chamado **Nova Aba**.  
  - Deve criar uma nova aba até o limite de **4 abas simultâneas**.  
  - Caso o limite seja atingido, exiba uma mensagem ao usuário.

### 2. **Remoção de Abas**
- Adicione um botão chamado **Fechar Aba**.  
  - Deve fechar a aba atualmente selecionada.  
  - Caso não existam abas abertas, exiba uma mensagem informativa.

### 3. **Leitura de Arquivo HTML**
- Adicione um botão chamado **Ler HTML**.  
  - Deve carregar o conteúdo de um arquivo `.txt` que contém um código HTML simulado.  
  - O conteúdo carregado será exibido em uma nova aba.

---

## 🛠️ Estrutura do Projeto

### 1. **Classe `HtmlLoader`**
Gerencia o carregamento de arquivos HTML simulados.  

- **Métodos:**  
  - `HtmlLoader(const std::string& filePath)`: Construtor que carrega o conteúdo de um arquivo.  
  - `std::string getContent() const`: Retorna o conteúdo carregado para exibição.  

- **Atributos:**  
  - `std::string content`: Armazena o conteúdo lido do arquivo.  

### 2. **Modificações na Classe `Tab`**
- Adicione um atributo `htmlContent` para armazenar o conteúdo carregado pelo `HtmlLoader`.  
- Modifique o método `draw` para exibir o conteúdo de `htmlContent`.  

### 3. **Modificações na Classe `BrowserWindow`**
- Implemente o botão **Nova Aba**: Cria novas abas até o limite.  
- Implemente o botão **Fechar Aba**: Remove a aba selecionada.  
- Implemente o botão **Ler HTML**: Usa o `HtmlLoader` para carregar o conteúdo de um arquivo e exibi-lo.

---

## 🌐 Estrutura do Código HTML Simulado

Aqui está um exemplo de código HTML simples para salvar em um arquivo `.txt` e utilizar no projeto:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página HTML</title>
</head>
<body>
    <h1>Título da Página</h1>
    <h2>Subtítulo da Página</h2>
    <p>Este é um parágrafo de exemplo que descreve o conteúdo da página.</p>
    <p>Mais um parágrafo para simular conteúdo adicional na página.</p>
</body>
</html>
