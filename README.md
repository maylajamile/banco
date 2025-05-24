# Aplicação Banco

Este sistema é responsável por fornecer os dados de transferências bancárias de acordo com o número de uma conta. É possível fazer uma busca mais completa por meio dos parâmetros <em>dataInicio</em> e <em>dataFinal</em> para determinar um período e por <em>operador </em>para buscar pelo nome do operador da transferência.

<img src="https://github.com/maylajamile/github-images/blob/041414446d872b86a4a95f58696d7142d7b2046f/image5.png" alt="Imagem da tela da aplicação"/>

<table>
<caption><strong>Url:</strong></caption>
  <thead>
    <tr>
      <th>Endpoint</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>http://localhost:8080/transferencias/{idConta}</td>
      <td>Listar todas as transferências de uma conta</td>
    </tr>
  </tbody>
</table>

## Banco de Dados

Este sistema carrega um banco de dados de teste em memória com os seguintes registros:

```sql
INSERT INTO conta (id_conta, nome_responsavel) VALUES (1,'Fulano');
INSERT INTO conta (id_conta, nome_responsavel) VALUES (2,'Sicrano');

INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (1,'2019-01-01 12:00:00+03',30895.46,'DEPOSITO', null, 1);
INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (2,'2019-02-03 09:53:27+03',12.24,'DEPOSITO', null,2);
INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (3,'2019-05-04 08:12:45+03',-500.50,'SAQUE', null,1);
INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (4,'2019-08-07 08:12:45+03',-530.50,'SAQUE', null,2);
INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (5,'2020-06-08 10:15:01+03',3241.23,'TRANSFERENCIA', 'Beltrano',1);
INSERT INTO transferencia (id,data_transferencia, valor, tipo, nome_operador_transacao, conta_id) VALUES (6,'2021-04-01 12:12:04+03',25173.09,'TRANSFERENCIA', 'Ronnyscley',2);
```

## Ferramentas

- JDK 17
- Spring Framework
- React.js
- H2 Database
- Maven
- IntelliJ IDEA
- VSCode

