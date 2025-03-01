# Expressões Regulares

Para finalizar qualquer regex, utiliza o caractere `$`.

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
    <td><code>12312312312</code></td>
    <td>apenas números</td>
  </tr>
  <tr>
    <td><code>/d{3}</code></td>
    <td><code>123.456.768-10</code></td>
    <td><code>123456789</code></td>
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
    <td><code>..-</code></td>
    <td>apenas ponto **OU** hífen</td>
  </tr>
</table>

