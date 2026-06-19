# Modelo de Dados

## Entidade: Sticker

Representa uma figurinha do álbum.

| Campo   | Tipo    | Obrigatório | Descrição                 | Restrição
|---------|---------|-------------|---------------------------| 
| id      | Long    | Sim         | Identificador único       | PK
| codigo  | String  | Sim         | Código da figurinha       | UNIQUE
| nome    | String  | Sim         | Nome do jogador           |
| selecao | String  | Sim         | Seleção/País              |
| imagem  | String  | Sim         | Nome do arquivo da imagem |
| quantidade | Int  | Sim         | Quantidade possuída       | >= 0
| paginas | String  | Sim         | Página do álbum           |

obs: PK = primary key
unique = unico
>= 0 = não possui numeros menores que zero
---

## Exemplo

id: 1
codigo: BRA-001
nome: Neymar Jr
selecao: Brasil
imagem: bra001.png
quantidade: 3
paginas: 14-15


Diagrama de classes UML

+--------------------------------+
|            Sticker             |
+--------------------------------+
| - id: Long (PK)                |
| - codigo: String (UNIQUE)      |
| - nome: String                 |
| - selecao: String              |
| - imagem: String               |
| - quantidade: Int              |
| - paginas: String              |
+--------------------------------+
