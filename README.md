# Expressões Regulares no Python

Neste repositório, vamos explorar o poder das expressões regulares em Python. Veremos como criar e testar expressões, bem como como usá-las para realizar buscas e substituições em strings. 

A biblioteca ***re*** do Python fornece várias funções úteis para trabalhar com expressões regulares e manipulação de strings. Dentre as funções mais comuns dessa biblioteca, estão ***split()***, ***sub()***, ***findall()*** e ***search()***, cada uma delas com suas próprias vantagens e benefícios.

O método ***split()*** é utilizado para quebrar uma string em partes menores, com base em um determinado padrão. Ele retorna uma lista contendo as partes da string que foram separadas. Por exemplo, você pode usar o método ***split()*** para quebrar uma string em palavras, com base em espaços em branco ou outros caracteres especiais.

```python
#!/usr/bin/python3

from re import split

# Separando por padrão (SPLIT)

texto = "Loreny sempre foi fascinada pela música e passava horas tocando piano em seu quarto."

lista_palavras = split(" ", texto)

print(lista_palavras)

dados_bancarios = "Banco: 341; Agência: 1234; Conta: 12345-6; Titular: João da Silva; Saldo: R$ 1000.00; Tipo: Corrente"

lista_dados_bancarios = split(";", dados_bancarios)

print(lista_dados_bancarios)

```

Já o método ***sub()*** é utilizado para substituir partes de uma string que correspondam a um determinado padrão. Ele retorna uma nova string com as substituições aplicadas. Isso é útil quando você precisa alterar ou corrigir informações em uma string, como substituir um texto específico por outro.

```python
#!/usr/bin/python3

from re import sub

# Substituindo Texto (SUB)

texto_para_substituir = r"Olá, Pedro! Tudo bem?"

novo_texto = sub("Pedro", "João", texto_para_substituir, count=1)

print(novo_texto)

```

O método ***findall()*** é utilizado para encontrar todas as ocorrências de um padrão em uma string e retorná-las como uma lista. Isso é útil para quando você precisa extrair informações específicas de uma string, como números de telefone ou endereços de e-mail.

```python
#!/usr/bin/python3

from re import findall

# Localizando padrões (FINDALL)

texto_com_telefones = """
(11) 1234-5678 é o número de telefone da minha casa.
Preciso ligar para o meu médico, o número é (21) 9876-5432.
Se quiser falar comigo, pode ligar no celular (47) 99876-5432.
O telefone da empresa é (19) 3456-7890, você pode ligar para o setor de atendimento.
Preciso falar com o meu advogado, o número dele é (51) 8765-4321.
"""

lista_de_telefones = findall("\(\d{2}\)\s\d{3,}-\d{3,}", texto_com_telefones)

print(lista_de_telefones)

```

Por fim, o método ***search()*** é utilizado para encontrar a primeira ocorrência de um padrão em uma string e retorná-la como um objeto de correspondência. Isso é útil quando você precisa de informações mais detalhadas sobre uma correspondência, como a posição em que ela ocorreu na string ou o comprimento da correspondência.

```python
#!/usr/bin/python3

from re import search

# Pesquisa (SEARCH)

texto_para_pesquisa = r"A máquina está ativa? SIM"

if search("SIM", texto_para_pesquisa):
    print("Sim, a máquina está ativa.")
else:
    print("Não, a máquina não está ativa.")

```

Em resumo, o uso desses métodos da biblioteca ***re*** do Python pode tornar a manipulação de strings e expressões regulares mais eficiente e eficaz. Eles permitem que você trabalhe com diferentes tipos de padrões e extraia informações específicas de uma string de forma mais fácil e precisa.

# Referência:

Re, ***Operações com expressões regulares***. Disponível em: <https://docs.python.org/pt-br/3/library/re.html>. Acesso em: 18 abr. 2023.