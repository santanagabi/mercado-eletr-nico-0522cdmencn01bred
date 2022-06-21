# Aula 13 - Coleção: Enum, Dictionary, Hashtable, SortedList e Iterador

## Resumo do conteúdo da aula

### Enum: Enumeradores

#### 1.1. Declarar / Popular

```cs
enum Dias { Segunda, Terca, Quarta, Quinta, Sexta };

enum Cores 
{
	Verde = 0xFF0000,
	Azul = 0x000FF,
    Amarelo = 0xFFFF00,
    Laranja = 0xFFA500,
    Roxo = 0xA020F0
}
```
#### 1.2. Acessar

```cs
Dias Disponibilidade = Dias.Segunda;
Cores Hexadecimal = Cores.Azul;
```

#### 1.3. Iterar

```cs
Array NomesDasCores = Enum.GetNames(typeof(Cores));
Array Hexadecimais = Enum.GetValues(typeof(Cores));

foreach (string cor in NomesDasCores)
{
	Console.WriteLine($"Nome da cor: {cor}");
}

foreach (string herexadecimal in Hexadecimais)
{
	Console.WriteLine($"Valor do código da cor: {herexadecimal}");
}
```

### Dictionary: Coleção de chave e valor

#### 1.1. Declarar

```cs
Dictionary<string, string> UF = new Dictionary<string, string>();
```
#### 1.2. Adicionar

```cs
UF.Add("RJ", "Rio de Janeiro");
UF.Add("SP", "São Paulo");
UF.Add("MG", "Minas Gerais");
```

#### 1.3. Acessar

```cs
string Estado = UF["RJ"];
```
ou 

```cs
UF.TryGetValue("RJ", out string Estado);
```

#### 1.4. Remover

```cs
UF.Remove("MG");
```

#### 1.5. Iterar

```cs
Dictionary<string, string> UF = new Dictionary<string, string>();
```

### Hashtable: Coleção de chave e valor

```cs

```

### SortedList: Coleção de chave e valor ordenada

```cs

```

### Iterator: Pecorrendo uma coleção

```cs

```

## Materiais de apoio

- Apresentações
	- [Coleção: Coleção: Enum, Dictionary, Hashtable, SortedList e Iterador](https://docs.google.com/presentation/d/1b2XABKOt22lPtaIyr6gZdPTaMjxT2tcO/edit?usp=sharing&ouid=105282487340930868863&rtpof=true&sd=true)
- Atividades
    - [Mesa de trabalho](https://docs.google.com/document/d/1fIpkgYOwnM8hIOVd3BgmTJgA49b3cFN8NeILyTl-OBE/edit?usp=sharing)
- Atividades resolvidas (Professor)
	- [Mesa de trabalho]()
- Atividade resolvida (Alunos)
	- [Mesa de trabalho](./ENTREGA.md)