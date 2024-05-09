# Estudos-React
É um template de estudos sobre React feito para o curso de Imersão em IA na Alura

## Conceitos Básicos do React

# Introdução

O React é uma biblioteca JavaScript declarativa, eficiente e flexível para criar interfaces de usuário. Ele permite a construção de interfaces complexas a partir de pequenos blocos de código reutilizáveis chamados "componentes".

Este guia apresenta os conceitos fundamentais do React para iniciantes:

## 1. Componentes

Componentes são os pilares do React. Eles são unidades independentes e reutilizáveis de código que representam partes da interface do usuário. Cada componente tem sua própria lógica e visualização, e pode ser composto por outros componentes menores.

### Tipos de Componentes

* **Componentes Funcionais:** Escritos como funções JavaScript que retornam JSX (uma extensão do HTML).
* **Componentes de Classe:** Definem uma classe JavaScript que estende a classe `React.Component`.

### Características dos Componentes

* **Reutilizáveis:** Componentes podem ser utilizados em diferentes partes da aplicação.
* **Componíveis:** Componentes podem ser compostos por outros componentes para criar interfaces complexas.
* **Isoláveis:** Mudanças em um componente não afetam outros componentes.

## 2. JSX

O JSX é uma sintaxe de extensão do HTML que permite escrever código HTML dentro do JavaScript. Ele facilita a criação de interfaces de usuário declarativas e legíveis.

### Exemplo de JSX

```javascript
function App() {
  return (
    <div className="App">
      <h1>Título da Aplicação</h1>
      <p>Um parágrafo de texto.</p>
    </div>
  );
}
```

### Características do JSX

* **Legível:** O JSX torna o código HTML mais fácil de entender e escrever.
* **Seguro:** O JSX é verificado no tempo de compilação para evitar erros.
* **Flexível:** O JSX pode ser usado com componentes, props e estado do React.

## 3. Props

Props (propriedades) são valores que são passados de um componente pai para um componente filho. Eles permitem que os componentes recebam e configurem seus comportamentos.

### Exemplo de Props

```javascript
function Greeting(props) {
  return (
    <h1>Olá, {props.nome}!</h1>
  );
}
```

### Características das Props

* **Passagem de dados:** Props permitem que os componentes pai forneçam dados aos componentes filho.
* **Configuração de componentes:** Props podem ser usadas para personalizar a aparência e o comportamento dos componentes.
* **Tipagem:** O React pode inferir tipos para props, tornando o código mais seguro e confiável.

## 4. Estado

O estado é um dado interno e mutável de um componente. Ele permite que os componentes armazenem e atualizem informações que afetam sua renderização.

### Exemplo de Estado

```javascript
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  handleClick() {
    this.setState((prevState) => ({ count: prevState.count + 1 }));
  }

  render() {
    return (
      <div>
        <p>Contagem: {this.state.count}</p>
        <button onClick={this.handleClick}>Incrementar</button>
      </div>
    );
  }
}
```

### Características do Estado

* **Armazenamento de dados:** O estado armazena informações relevantes para o componente.
* **Atualização da interface:** Mudanças no estado re-renderizam o componente com a nova informação.
* **Gerenciamento de interações:** O estado é usado para gerenciar interações do usuário e eventos.

## 5. Hooks

Hooks são funções especiais que permitem usar o estado e outros recursos do React sem escrever classes. Eles facilitam o compartilhamento de lógica entre componentes e simplificam o código.

### Exemplo de Hook

```javascript
function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Contagem: {count}</p>
      <button onClick={() => setCount(count + 1)}>Incrementar</button>
    </div>
  );
}
```

### Características dos Hooks

* **Simplificação do código:** Hooks eliminam a necessidade de classes, tornando o código mais conciso e legível.
* **Reuso de lógica:** Hooks podem ser reutilizados entre diferentes componentes.
* **Gerenciamento de estado:** Hooks facilitam o gerenciamento do estado do componente.

## 6. Virtual DOM

O React utiliza um DOM virtual para otimizar.
