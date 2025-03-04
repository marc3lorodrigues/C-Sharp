# C-Sharp
Repositório destinado a conteúdos sobre C#.

## 1. Criando uma nova solução
Para criar uma nova solução através do terminal deverá ser escolhido um template.

### 1.1 Escolhendo um tamplate
~~~powershell
dotnet new list
~~~

### 1.2 Criando uma solução
Para criar uma nova solução basta usar o template e nomear a solução.
Exemplo:
~~~powershell
dotnet new sln -n Fundamentos
~~~
## 2. Criando um projeto
Para criar um novo projeto deve ser informado o tipo de projeto, o nome e o framework.
Exemplo:
~~~powershell
dotnet new console -n Appconsole -f net6.0
~~~

### 2.1 Adicionando um projeto em uma solução
Para adicionar um projeto em uma solução deverá ser indicado a solução e o projeto a ser colocado.
Exemplo:
~~~powershell
dotnet sln Fundamentos.sln add AppConsole
~~~

### 2.2 Compilando um projeto
Para compilar todos os projetos da solução basta utilizar o comando confirme exemplo.
Exemplo:
~~~powershell
dotnet build
~~~

### 2.3 Limpando arquivos de compilação
Para limpar arquivos gerados na compilação basta utilizar o comando clean.

Exemplo:
~~~powershell
dotnet clean
~~~

## 3. Executando um projeto
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

## 4. Tipo de Dados
A microsoft fornece uma tabela com os referidos tipos. O conteúdo pode ser acessado no link [Tipos de dado](https://learn.microsoft.com/pt-br/dotnet/csharp/language-reference/builtin-types/value-types).

## 4.1 Estrutura de Dados
É uma forma de agrupar dados que possuem a mesmas características.

### 4.1.1 ArrayList
Armazena uma lista de dados de qualquer tipo, ou seja, texto, numero e etc.

#### Criando uma lista
~~~csharp
var lista = new ArrayList();   
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
#### Deletando um item da lista
~~~csharp
lista.RemoveAt(0);
~~~

### 4.1.2 Array Tipado
Armazena uma lista de dados do mesmo tipo. O tamanho deve ser definido na criação da lista.

#### Criando uma lista
~~~csharp
var ListaTipada = new int[3] {1,3,5};
~~~
#### Definindo o valor da lista
~~~csharp
ListaTipada[0] = 25;
~~~

#### Recuperando o valor da lista
~~~csharp
var valor = ListaTipada[2];
Console.WriteLine(valor);
~~~

#### Imprimindo toda lista
~~~csharp
foreach (var item in ListaTipada)
    Console.WriteLine(item);
~~~

### 4.1.3 Lista Genérica
Armazena uma lista de dados do de qualquer lista. Apesar de poder ser definido um tamanho inicial a lista possui métodos para adição e remoção de elementos. 

#### Criando uma lista com tamanho definido
~~~csharp
var lista = new List<string>(10);
~~~
#### Criando uma lista com tamanho genérico
~~~csharp
var listaGenerica = new List<string>();
~~~

#### Adicionando itens na lista
~~~csharp
listaGenerica.Add("C#");
listaGenerica.Add("Java");
listaGenerica.Add("JScript");
listaGenerica.Add("CSS");
listaGenerica.Add("HTML");
~~~

#### Lendo um item da lista
~~~csharp
var item = listaGenerica[4];
console.writeLine(item);
~~~

#### Imprimindo todos os itens da lista
~~~csharp
foreach (var item in listaGenerica)
    Console.WriteLine(item);
~~~

#### Excluindo um elemento da lista
~~~csharp
listaGenerica.RemoveAt(2);
~~~

#### Contando os elementos da lista
~~~csharp
listaGenerica.Count();
~~~

#### Limpando a lista
~~~csharp
listaGenerica.Clear();
~~~


### 4.1.4 Dicionario
Representa uma coleção de itens com chave/valor.

Definindo uma Lista.
~~~csharp
Dictionary<int, string> dic = 
    new Dictionary<int, string>();
~~~

Adicionando valores
~~~csharp
dic.Add(1,"Oracle");
dic.Add(2,"MySql");
dic.Add(3,"SqlServer");
dic.Add(4,"Postgress");
dic.Add(5,"MariaDB");
~~~

definindo um valor para uma chave
~~~csharp
dic[3] = "Access";
~~~

Recuperando o valor de uma chave
~~~csharp
var nome = dic[3];
Console.WriteLine(nome);
~~~

Imprimindo itens
~~~csharp
foreach (var item in dic)
  Console.WriteLine("A chave {0} possui o valor {1}.",item.Key,item.Value);  
~~~



