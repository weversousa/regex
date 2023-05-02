# RegEx (Regular Expression)

Identificra caracteres (um padrão) em texto.

Extrair ao encontrar um padrão.

Achar um padrão e trocar por outro padrão.

---

## Símbolos

| SÍMBOLO  | DESCRIÇÃO                                            |
| :-       | :-                                                   |
| .        | qualquer caractere exceto nova linha/linha em branco |
| \w \d \s | letra ou número ou _, número, espaço em branco       |
| \W \D \S | negação                                              |
| [abc]    | caractere a, b ou c                                  |
| [^abc]   | qualquer caractere diferente de a, b ou c            |
| [a-z]    | qualquer caractere entre a e z                       |
| [A-Z]    | qualquer caractere entre A e Z                       |
| [a-zA-Z] | qualquer caractere entre a e z ou A e Z              |
| ^abc     | sequência abc exatamente no início da string         |
| abc$     | sequência abc exatamente no fim da string            |
| ^abc$    | sequência abc exatamente igual a string              |
| \. \* \\ | escapar caracter especial                            |
| \t \n \r | tab, quebra de linha, retorno ao começo da linha     |
| a* a+ a? | 0 ou mais a, 1 ou mais a, 0 ou 1 a                   |
| a{5}     | exatamente 5 caracteres a seguidos                   |
| a{2,}    | 2 ou mais caracteres a seguidos                      |
| a{1,3}   | entre 1 e 3 caracteres a seguidos                    |
| ab|cd    | sequência ab ou cd                                   |

---

## Grupos

Podemos separar padrões usando parênteses, e assim  formar grupos para manipular as partes encontradas.

Cada grupo da esquerda para a direita é representado por um número começando em 1.

Esse número é usado para acessar o grupo após a consulta.

No VS Code por exemplo, é **$1** **$2** **$3**...

Exemplo:

texto = "2023-05-02 11:39:00"

padrao = `([0-9]{4})[-]([0-9]{2})[-]([0-9]{2})`  
            **$1           $2           $3**

Ao aplicar `$3/$2/$1`:
novo_texto = "02/05/2023 11:39:00"
