# Princípio da Responsabilidade Única (SRP)
  O Princípio da Responsabilidade Única (SRP) é um dos princípios fundamentais da programação orientada a objetos. Ele estabelece que uma classe deve ter apenas uma única responsabilidade, ou seja, deve ter um único motivo para mudar.

Ao seguir o SRP, o código do projeto se torna mais coeso, mais fácil de entender e de manter. Cada classe é especializada em uma única tarefa ou funcionalidade, o que facilita a compreensão do código e reduz o acoplamento entre as classes.

Ao dividir as responsabilidades em classes distintas, torna-se mais simples fazer modificações no sistema, pois as mudanças afetam apenas a classe relevante. Isso ajuda a evitar efeitos colaterais indesejados e simplifica a manutenção do código no longo prazo.

Seguir o Princípio da Responsabilidade Única promove um código mais organizado, modular e flexível, contribuindo para um desenvolvimento mais eficiente e sustentável do projeto.

```csharp
using System;

// Classe responsável por manipular dados de um estudante
public class Estudante
{
    public string Nome { get; set; }
    public int Idade { get; set; }
    public int Matricula { get; set; }
}

// Classe responsável por persistir os dados do estudante em um banco de dados
public class EstudanteRepository
{
    public void SalvarEstudante(Estudante estudante)
    {
        // Lógica para salvar o estudante no banco de dados
        Console.WriteLine("Estudante salvo no banco de dados.");
    }
}

// Classe responsável por exibir informações sobre o estudante
public class EstudanteInfoPrinter
{
    public void ImprimirInformacoes(Estudante estudante)
    {
        // Lógica para imprimir as informações do estudante
        Console.WriteLine($"Nome: {estudante.Nome}");
        Console.WriteLine($"Idade: {estudante.Idade}");
        Console.WriteLine($"Matrícula: {estudante.Matricula}");
    }
}

// Classe principal
public class Program
{
    public static void Main()
    {
        Estudante estudante = new Estudante
        {
            Nome = "João",
            Idade = 20,
            Matricula = 12345
        };

        EstudanteRepository repository = new EstudanteRepository();
        repository.SalvarEstudante(estudante);

        EstudanteInfoPrinter printer = new EstudanteInfoPrinter();
        printer.ImprimirInformacoes(estudante);
    }
}
```

## Livro
![Imagem](https://m.media-amazon.com/images/I/51YTqGVOD7L._SY425_.jpg)

# Autor
Thiago Reis Lima
https://www.linkedin.com/in/thiago-lima-2a5896166/
