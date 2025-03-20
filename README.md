# Expressões Regulares

Para finalizar qualquer regex, utiliza o caractere `$`;<br/>
Para incluir espaços em branco, utiliza o `\s` e para não incluir `\S`;<br/>
Para incluir todos os caracteres, utiliza o `.*`.

## Números

<table>
  <tr>
    <th>regex</th>
    <th>input</th>
    <th>output</th>
    <th>explicação</th>
  </tr>
  <tr>
    <td><code>/d</code></td>
    <td><code>123.123.123-12</code></td>
    <td><code>1 2 3 1 2 3 1 2 3 1 2</code></td>
    <td>apenas números</td>
  </tr>
  <tr>
    <td><code>/d{3}</code></td>
    <td><code>123.456.768-10</code></td>
    <td><code>123 456 789</code></td>
    <td>apenas agrupamentos de 3 números</td>
  </tr>
  <tr>
    <td><code>^/d{3}</code></td>
    <td><code>123.456.768-10</code></td>
    <td><code>123</code></td>
    <td>apenas o primeiro agrupamento de 3 números</td>
  </tr>
</table>

## Operações lógicas

<table>
  <tr>
    <th>regex</th>
    <th>input</th>
    <th>output</th>
    <th>explicação</th>
  </tr>
   <tr>
    <td><code>[.-]</code></td>
    <td><code>123.123.123-12</code></td>
    <td><code>. . -</code></td>
    <td>apenas ponto <strong>OU</strong> hífen</td>
  </tr>
</table>

## Letras e/ou Palavras

<table>
  <tr>
    <th>regex</th>
    <th>input</th>
    <th>output</th>
    <th>explicação</th>
  </tr>
  <tr>
    <td><code>/w</code></td>
    <td><code>Gabriel, 26</code></td>
    <td><code>G a b r i e l 2 6</code></td>
    <td>apenas letras e números, excluindo símbolos</td>
  </tr>
  <tr>
    <td><code>/w+</code></td>
    <td><code>Gabriel, 26</code></td>
    <td><code>Gabriel 26</code></td>
    <td>agrupamentos de letras e números</td>
  </tr>
</table>

## Grupos

<table>
  <tr>
    <th>regex</th>
    <th>input</th>
    <th>output</th>
    <th>explicação</th>
  </tr>
  <tr>
    <td><code>^(\w+),\s\w+,\s(\w+)$</code></td>
    <td><code>Azevedo, 26, Gabriel</code></td>
    <td>Grupo 01: <code>Azevedo</code> Grupo 02: <code>Gabriel</code></td>
    <td>criar grupos dentro do regex, os mesmos eventualmente poderam ser utilizadas como <a href="#### Utilizando grupo como parâmetro">parâmetros</a></td>
  </tr>
</table>

#### Utilizando grupo como parâmetro

<div>
  <img src="https://github.com/user-attachments/assets/916c35ef-4cfa-4a50-b54f-c59a9cf0b2c4" height="80px"/>
  <img src="https://github.com/user-attachments/assets/762abf78-55f5-4072-994c-4dbd3e58b13e" height="80px"/>
</div>

## Flags

- `g` global: Não retorna depois do primeiro acerto
- `i` insensitive: Considera texto maiúsculo ou minúsculo
- `m` multiline: Considerar múltiplas linhas na pesquisa




