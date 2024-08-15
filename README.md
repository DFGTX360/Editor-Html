# Editor de Texto em C#

Este é um projeto de um editor de texto simples desenvolvido em C#. Ele permite criar e visualizar arquivos de texto com destaque de palavras em `strong` em HTML. O editor possui um menu interativo que permite ao usuário iniciar um novo arquivo ou visualizar um arquivo existente.

## Funcionalidades

- Criação de novos arquivos de texto
- Visualização de arquivos com destaque em HTML (`<strong>`)
- Interface simples com opções de menu
- Modo de edição e visualização com suporte a cores no console

## Como usar

1. Clone este repositório:
    ```bash
    git clone https://github.com/DFGTX360/EditorTextoCSharp.git
    ```
2. Abra o projeto em sua IDE de C# preferida (Visual Studio ou Visual Studio Code).
3. Compile e execute o projeto.
4. Siga as instruções no console para criar ou visualizar um arquivo.

## Estrutura do Código

O projeto está dividido em classes que controlam o menu, a edição de texto e a visualização de texto. Cada classe tem uma responsabilidade específica para manter o código organizado.

### Classe `Menu`

A classe `Menu` exibe as opções disponíveis para o usuário no console e controla o fluxo do programa. O usuário pode selecionar entre as opções de criar um novo arquivo, abrir um arquivo existente, ou sair do programa.

### Classe `Editor`

A classe `Editor` é responsável por iniciar o modo de edição, onde o usuário pode escrever texto diretamente no console. O texto é salvo em um objeto `StringBuilder` até que o usuário pressione a tecla `Esc`.

### Classe `Viewer`

A classe `Viewer` exibe o conteúdo do texto digitado no modo de edição, com suporte para destaque de palavras que estão dentro de tags `<strong>` em HTML. O texto é renderizado com cores diferentes no console, simulando uma visualização de HTML.

## Exemplo de Uso

Ao iniciar o programa, o usuário verá um menu com as seguintes opções:

```bash
1 - Novo arquivo
2 - Abrir
3 - Sair

*----------------------------------------------*
internal class Program
{
    private static void Main(string[] args)
    {
        Menu.Show();
    }
}

*---------------------------------------------*

public static class Menu
{
    public static void Show()
    {
        Console.Clear();
        DrawScreen();
        WriteOptions();
        
        var option = short.Parse(Console.ReadLine());
        HandleMenuOption(option);
    }
    
    // Outros métodos da classe...
}

*---------------------------------------------------*

public static class Editor
{
    public static void Show()
    {
        Console.Clear();
        Start();
    }

    // Outros métodos da classe...
}

*---------------------------------------------------*

public class Viewer
{
    public static void Show(string text)
    {
        Console.Clear();
        Replace(text);
        Menu.Show();
    }
    
    // Outros métodos da classe...
}

*------------------------------------------------*.


Esse README oferece uma boa visão geral do projeto e orienta os usuários sobre como utilizá-lo e contribuir. Se precisar de algo mais específico, estou à disposição!


