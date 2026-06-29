# Criptografia
---
## Área de Estudo: Redes e Segurança da Informação
---
## Explicação

Criptografia é o conjunto de técnicas para proteger informações,
garantindo que apenas as partes autorizadas possam acessá-las.

**Criptografia Simétrica**
- Usa a **mesma chave** para encriptar e decriptar
- Mais rápida, porém exige que remetente e destinatário compartilhem
  a chave de forma segura previamente
- Exemplo de algoritmo: AES (Advanced Encryption Standard)

**Criptografia Assimétrica**
- Usa um **par de chaves**: uma pública e uma privada
- A chave pública pode ser compartilhada livremente
- A chave privada nunca é compartilhada
- O que é encriptado com a chave pública só pode ser decriptado com
  a chave privada correspondente, e vice-versa
- Usada para verificar autenticidade e estabelecer comunicações seguras
- Exemplo de algoritmo: RSA

**Vetor de Inicialização (IV)**
- Valor aleatório combinado com a chave antes da encriptação
- Garante que a mesma mensagem encriptada em momentos diferentes
  produza resultados diferentes
- Oculta padrões nos dados encriptados
- Impede ataques de reprodução, em que um atacante captura e reenvia
  uma mensagem válida para enganar o destinatário

**Função de Hash Criptográfico**
- Gera um valor de tamanho fixo a partir de qualquer mensagem
- Qualquer alteração na mensagem, por menor que seja, gera um hash
  completamente diferente
- Usado para verificar a **integridade** das mensagens
- Não é possível recuperar a mensagem original a partir do hash
  (função de mão única)
- Exemplo de algoritmo: SHA-256

**Propriedades de segurança da informação**
- **Confidencialidade:** apenas partes autorizadas acessam a informação
- **Integridade:** a informação não foi alterada durante a transmissão
- **Autenticidade:** a identidade do remetente é verificada

**Ponto importante**
AES é criptografia **simétrica** (mesma chave para encriptar e
decriptar). RSA é criptografia **assimétrica** (par de chaves pública
e privada). SHA-256 é uma função de **hash**, não um algoritmo de
criptografia, pois não permite recuperar a mensagem original.

---
## Referências

- [Criptografia](https://www.ibm.com/br-pt/think/topics/cryptography)

---
## Questões Relacionadas

- [[Questão 24]]

---
## Conceitos Relacionados

- [[]]