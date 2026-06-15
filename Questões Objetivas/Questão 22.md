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

## Resposta

> **Letra A**
## Explicação