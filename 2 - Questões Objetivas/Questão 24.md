## Questão 24

### Texto

A criptografia de ponta a ponta do WhatsApp garante que somente você e a pessoa com quem você está se comunicando podem ler o que é enviado. Ninguém mais terá acesso a elas, nem mesmo o WhatsApp. As suas mensagens estão seguras com cadeados e somente você e a pessoa que as recebe possuem as chaves especiais necessárias para abri-los e ler as mensagens. E, para uma proteção ainda maior, cada mensagem que você envia tem um cadeado e uma chave únicos.

> Disponível em: https://faq.whatsapp.com/pt_br/general/28030015. Acesso em: 05 mai. 2020.

---

## Enunciado

Com base no texto acima e considerando os conceitos de segurança e criptografia, avalie as afirmações a seguir.

> **I.** Se um par de chaves é gerado durante a instalação do aplicativo e a chave pública do usuário é armazenada no servidor, é possível verificar a autenticidade de uma mensagem recebida usando a chave pública do remetente obtida do servidor.

> **II.** A estratégia de utilizar um vetor de inicialização (IV) variável para compor chaves criptográficas diferentes para cada mensagem enviada oculta padrões de dados, além de dificultar os chamados ataques de reprodução.

> **III.** O uso do algoritmo AES nas comunicações entre dois usuários indica o emprego de criptografia simétrica, isto é, aquela que utiliza um par de chaves, uma usada pelo remetente, para encriptar a mensagem, e outra para o destinatário decriptá-la.

> **IV.** A presença do algoritmo SHA-256, no protocolo de comunicação entre cliente e servidor, sugere a verificação de integridade das mensagens, visto que é possível detectar se ocorreu alguma modificação comparando-se os valores de *hash* da mensagem enviada e recebida.

É correto apenas o que se afirma em

- **A)** I e IV.
- **B)** II e III.
- **C)** III e IV.
- **D)** I, II e III.
- **E)** I, II e IV.
---
## Resposta

> **Letra E**

---
## Explicação


A afirmação I é verdadeira. Em criptografia assimétrica, cada usuário possui um par de chaves: uma pública e uma privada. A chave pública pode ser armazenada em um servidor e consultada por qualquer pessoa. Para verificar a autenticidade de uma mensagem, o receptor usa a chave pública do remetente obtida do servidor para confirmar que a mensagem foi assinada com a chave privada correspondente, que só o remetente possui.

A afirmação II é verdadeira. O vetor de inicialização (IV) é um valor aleatório combinado com a chave para garantir que a mesma mensagem encriptada em momentos diferentes produza resultados diferentes. Isso oculta padrões nos dados encriptados e impede ataques de reprodução, em que um atacante captura e reenvia uma mensagem válida para enganar o destinatário.

A afirmação III é falsa. O AES é de fato um algoritmo de criptografia simétrica. Criptografia simétrica usa a **mesma chave** tanto para encriptar quanto para decriptar a mensagem. A alternativa descreve o uso de chaves diferentes para encriptar e decriptar, o que é a definição de criptografia **assimétrica**, não simétrica.

A afirmação IV é verdadeira. O SHA-256 é uma função de hash criptográfico. Ele gera um valor fixo a partir de uma mensagem, e qualquer alteração na mensagem, por menor que seja, produz um hash completamente diferente. Por isso, comparar o hash da mensagem enviada com o da mensagem recebida permite detectar se houve alguma modificação, garantindo a integridade da comunicação.


---
## Conceitos Relacionados

- [[Criptografia]]