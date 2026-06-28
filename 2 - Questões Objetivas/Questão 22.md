## Questão 22

### Texto

Uma Organização Não Governamental (ONG), relacionada à causa animal, registra os *pets* (animais de estimação) amparados por ela, de acordo com o seguinte Diagrama Entidade Relacionamento (DER).

![[der-ong-pets.png]]

---

## Enunciado

A partir das regras de mapeamento do Modelo Conceitual para o Modelo Lógico Relacional, assinale o Esquema Relacional mais adequado a ser gerado. Considere que as chaves primárias estão sublinhadas.

- **A)**
  - `PESSOA(`<u>cpf</u>`: texto, nome: texto)`
  - `TIPO_PET(`<u>codigo</u>`: inteiro, descricao: texto)`
  - `PET(`<u>codigo</u>`: inteiro, nome: texto, data_nascimento: data, codigo_tipo_pet: inteiro, adotante: texto)`
    - `codigo_tipo_pet referencia TIPO_PET(codigo)`
    - `adotante referencia PESSOA(cpf)`

- **B)**
  - `PET(`<u>codigo</u>`: inteiro, nome: texto, data_nascimento: data)`
  - `PESSOA(`<u>cpf</u>`: texto, nome: texto, codigo_pet: inteiro)`
    - `codigo_pet referencia PET(codigo)`
  - `TIPO_PET(`<u>codigo</u>`: inteiro, descricao: texto, codigo_pet: inteiro)`
    - `codigo_pet referencia PET(codigo)`

- **C)**
  - `TIPO_PET(`<u>codigo</u>`: inteiro, descricao: texto)`
  - `PET(`<u>codigo</u>`: inteiro, nome: texto, data_nascimento: data, codigo_tipo_pet: inteiro)`
    - `codigo_tipo_pet referencia TIPO_PET(codigo)`
  - `PESSOA(`<u>cpf</u>`: texto, nome: texto, codigo_pet: inteiro)`
    - `codigo_pet referencia PET(codigo)`

- **D)**
  - `PET_PESSOA(`<u>codigo_pet</u>`: inteiro, nome_pet: texto, data_nascimento: data, cpf: texto, nome_pessoa: texto, codigo_tipo_pet: inteiro, descricao_tipo_pet: texto)`

- **E)**
  - `PESSOA(`<u>cpf</u>`: texto, nome: texto)`
  - `PET(`<u>codigo</u>`: inteiro, nome: texto, data_nascimento: data, codigo_tipo_pet: inteiro, descricao_tipo_pet, adotante: texto)`
    - `adotante referencia PESSOA(cpf)`

---
## Resposta

> **Letra A**

---
## Explicação

Para responder esta questão é necessário analisar o DER e aplicar as regras de mapeamento para o modelo relacional.

O DER apresenta três entidades: PESSOA, PET e TIPO_PET, com dois relacionamentos:

- **pertencer:** entre TIPO_PET e PET, com cardinalidade (1,1) para PET e (1,n) para TIPO_PET. Isso significa que cada PET pertence a exatamente um TIPO_PET, mas um TIPO_PET pode ter vários PETs.
- **adotar:** entre PESSOA e PET, com cardinalidade (1,1) para PESSOA e (0,n) para PET. Isso significa que cada PET pode ter no máximo um adotante, e uma PESSOA pode adotar vários PETs.

Pela regra de mapeamento, quando a cardinalidade é (1,1) de um lado, a chave estrangeira fica na tabela desse lado. Portanto a tabela PET recebe tanto a chave de TIPO_PET quanto a chave de PESSOA (adotante). Isso corresponde exatamente à alternativa A.

A alternativa B é falsa. Coloca a chave estrangeira de PET dentro de PESSOA e de TIPO_PET, o que inverteria a direção correta do relacionamento.

A alternativa C é falsa. Trata corretamente o relacionamento entre PET e TIPO_PET, mas erra no relacionamento entre PET e PESSOA ao colocar a chave de PET dentro de PESSOA, invertendo a direção.

A alternativa D é falsa. Junta todas as entidades em uma única tabela, o que viola as regras de normalização e gera redundância de dados.

A alternativa E é falsa. Coloca a descrição do tipo do pet diretamente na tabela PET em vez de usar uma chave estrangeira para TIPO_PET, eliminando a entidade TIPO_PET do esquema e gerando redundância.
