# Regras de Negócio – Álbum Digital Copa 2026

## Versão

1.1

## Autor

Pedro Freitas

## Objetivo

Este documento descreve as regras de negócio do aplicativo Álbum Digital Copa 2026, responsável pelo gerenciamento da coleção de figurinhas do usuário, controle de figurinhas repetidas, consulta de figurinhas faltantes e acompanhamento do progresso do álbum.

---

# RN01 - Quantidade de Figurinhas

## Descrição

O sistema utilizará um único campo chamado quantidade para representar o número total de cópias que o usuário possui de uma determinada figurinha.

## Regras

| Quantidade | Significado                               |
| ---------- | ----------------------------------------- |
| 0          | Não possui a figurinha                    |
| 1          | Possui a figurinha colada no álbum        |
| 2          | Possui 1 figurinha no álbum + 1 repetida  |
| 3          | Possui 1 figurinha no álbum + 2 repetidas |
| 4          | Possui 1 figurinha no álbum + 3 repetidas |

---

# RN02 - Figurinha Faltante

## Descrição

Uma figurinha será considerada faltante quando o usuário não possuir nenhuma cópia dela.

## Condição

Quantidade = 0

---

# RN03 - Figurinha Obtida

## Descrição

Uma figurinha será considerada obtida quando o usuário possuir pelo menos uma cópia dela.

## Condição

Quantidade >= 1

---

# RN04 - Figurinha Repetida

## Descrição

Uma figurinha será considerada repetida quando o usuário possuir mais de uma cópia dela.

## Condição

Quantidade >= 2

---

# RN05 - Quantidade de Repetidas

## Descrição

O número de figurinhas repetidas não será armazenado diretamente no banco de dados.

Ele será calculado automaticamente.

## Fórmula

Repetidas = Quantidade - 1

## Exemplos

| Quantidade | Repetidas |
| ---------- | --------- |
| 0          | 0         |
| 1          | 0         |
| 2          | 1         |
| 3          | 2         |
| 4          | 3         |

---

# RN06 - Filtro Todas

## Descrição

O filtro "Todas" deverá exibir todas as figurinhas cadastradas no álbum.

---

# RN07 - Filtro Faltantes

## Descrição

O filtro "Faltantes" deverá exibir apenas as figurinhas ainda não obtidas.

## Condição

Quantidade = 0

---

# RN08 - Filtro Repetidas

## Descrição

O filtro "Repetidas" deverá exibir apenas figurinhas disponíveis para troca.

## Condição

Quantidade >= 2

---

# RN09 - Progresso do Álbum

## Descrição

O sistema deverá calcular automaticamente o percentual de conclusão do álbum.

## Fórmula

Progresso = (Figurinhas Obtidas ÷ Total de Figurinhas) × 100

---

# RN10 - Estatísticas do Álbum

## Descrição

O sistema deverá apresentar indicadores sobre a coleção.

## Informações exibidas

* Total de figurinhas
* Figurinhas obtidas
* Figurinhas faltantes
* Figurinhas repetidas
* Percentual de progresso

---

# RN11 - Incremento de Quantidade

## Descrição

Ao pressionar o botão "+" o sistema deverá aumentar a quantidade da figurinha em uma unidade.

---

# RN12 - Decremento de Quantidade

## Descrição

Ao pressionar o botão "-" o sistema deverá reduzir a quantidade da figurinha em uma unidade.

---

# RN13 - Quantidade Mínima

## Descrição

O sistema não deverá permitir quantidades negativas.

## Valor mínimo permitido

0

---

# RN14 - Pesquisa de Figurinha

## Descrição

O usuário poderá pesquisar uma figurinha utilizando seu código.

## Exemplos

* BRA-001
* BRA-015
* ARG-022
* MEX-010

---

# RN15 - Código da Figurinha

## Descrição

Cada figurinha deverá possuir um identificador único.

## Estrutura

SIGLA DA SELEÇÃO + NÚMERO

## Exemplos

* BRA-001
* BRA-002
* ARG-001
* ARG-002
* MEX-001
* MEX-002

## Restrição

Não poderão existir duas figurinhas com o mesmo código.

---

# RN16 - Exibição das Figurinhas

## Descrição

Cada figurinha deverá exibir:

* Código
* Imagem
* Quantidade

## Exemplo

BRA-001

[Imagem da Figurinha]

* 03 +

---

# RN17 - Persistência dos Dados

## Descrição

Todas as alterações realizadas pelo usuário deverão ser armazenadas permanentemente no banco de dados local.

---

# RN18 - Inicialização do Álbum

## Descrição

Ao instalar o aplicativo pela primeira vez, todas as figurinhas deverão ser cadastradas automaticamente.

## Valor Inicial

Quantidade = 0

---

# RN19 - Atualização Automática das Estatísticas

## Descrição

Sempre que a quantidade de uma figurinha for alterada, o sistema deverá recalcular automaticamente:

* Figurinhas obtidas
* Figurinhas faltantes
* Figurinhas repetidas
* Percentual de progresso

---

# RN20 - Navegação por Seleção

## Descrição

O usuário poderá navegar pelas seleções participantes da Copa.

## Exemplos

* Brasil
* Argentina
* México
* Estados Unidos
* França
* Portugal

## Resultado Esperado

Ao selecionar uma seleção, o sistema deverá exibir apenas as figurinhas pertencentes àquela equipe.

---

# RN21 - Visualização dos Detalhes da Figurinha

## Descrição

Ao clicar ou tocar em uma figurinha na tela principal, o sistema deverá exibir uma tela de detalhes contendo informações completas da figurinha selecionada.

## Objetivo

Permitir que o usuário consulte rapidamente informações da figurinha sem precisar procurar manualmente no álbum físico.

## Informações Exibidas

* Código
* Nome
* Seleção
* Imagem
* Quantidade
* Página(s) do álbum

## Exemplo

Código: BRA-001

Nome: Neymar Jr

Seleção: Brasil

Imagem: bra001.png

Quantidade: 3

Página(s): 14-15

---

# RN22 - Localização da Figurinha no Álbum

## Descrição

Toda figurinha deverá possuir a informação da página ou intervalo de páginas onde ela está localizada no álbum físico.

## Objetivo

Facilitar a localização da figurinha durante a colagem, conferência e troca de figurinhas.

## Formatos Permitidos

Página única:

14

Intervalo de páginas:

14-15

Página dupla:

24-25

## Exemplos

| Código  | Nome              | Página |
| ------- | ----------------- | ------ |
| BRA-001 | Neymar Jr         | 14-15  |
| BRA-002 | Vinícius Jr       | 14-15  |
| ARG-001 | Messi             | 18-19  |
| POR-001 | Cristiano Ronaldo | 22-23  |

## Restrição

Toda figurinha cadastrada deverá possuir a informação de página preenchida.

---

# Considerações Finais

Estas regras representam a versão inicial do MVP (Minimum Viable Product) do Álbum Digital Copa 2026 e poderão ser ampliadas em futuras versões para suportar funcionalidades como:

* Login de usuário
* Sincronização em nuvem
* Compartilhamento de coleção
* Comparação de coleções
* Troca de figurinhas entre usuários
* Notificações
* Estatísticas avançadas

---

# Aprovação

Projeto: Álbum Digital Copa 2026

Autor: Pedro Freitas

Versão: 1.1
