# C-Sharp
Repositório destinado a conteúdos sobre C#.

## Criando uma nova solução
Para criar uma nova solução através do terminal deverá ser escolhido um template.

### Escolhendo um tamplate
~~~powershell
dotnet new list
~~~

### Criando uma solução
Para criar uma nova solução basta usar o template e nomear a solução.
Exemplo:
~~~powershell
dotnet new sln -n Fundamentos
~~~
## Criando um projeto
Para criar um novo projeto deve ser informado o tipo de projeto, o nome e o framework.
Exemplo:
~~~powershell
dotnet new console -n Appconsole -f net6.0
~~~

### Adicionando um projeto em uma solução
Para adicionar um projeto em uma solução deverá ser indicado a solução e o projeto a ser colocado.
Exemplo:
~~~powershell
dotnet sln Fundamentos.sln add AppConsole
~~~

### Compilando um projeto
Para compilar todos os projetos da solução basta utilizar o comando confirme exemplo.
Exemplo:
~~~powershell
dotnet build
~~~

### Limpando arquivos de compilação
Para limpar arquivos gerados na compilação basta utilizar o comando clean.

Exemplo:
~~~powershell
dotnet clean
~~~

## Executando um projeto
Para Executar um projeto deverá ser utilizado o comando run com o parâmetro --project caso esteja na pasta da solução. Uma outra alternativa e acessar a pasta do projeto e executar sem o parâmetro.

Exemplo 1:
~~~powershell
dotnet run --project Appconsole
~~~
Exemplo 2:
~~~powershell
cd Appconsole
dotnet run Appconsole
~~~

## Tipo de Dados
A microsoft fornece uma tabela com os referidos tipos. O conteúdo pode ser acessado no link [Tipos de dado](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/builtin-types/value-types).

## Estrutura de Dados
É uma forma de agrupar dados que possuem a mesmas características.

### ArrayList
Armazena uma lista de dados de qualquer tipo, ou seja, texto, numero e etc.

#### Criando uma lista
~~~csharp
var lista = new ArrayList();    // Cria um objeto de lista.
~~~
#### Adicionando um item na lista
~~~csharp
lista.Add(1);                   
lista.Add("Linguagem");         
lista.Add(true);               
~~~
#### Acessando um item da lista
~~~csharp
var item = lista[1];
~~~
#### deletando um item da lista
~~~csharp
lista.RemoveAt(0);
~~~

### Array Tipado
Armazena uma lista de dados do mesmo tipo.













