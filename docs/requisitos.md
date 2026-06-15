# Documento de Requisitos

## 1. Identificação do Projeto

Nome do Projeto: Álbum Digital da Copa
Versão: 1.0
Autor: Pedro Freitas
Data: Junho/2026

---

## 2. Objetivo

Desenvolver um aplicativo Android que permita aos colecionadores de figurinhas da Copa do Mundo controlar sua coleção digitalmente, registrando figurinhas obtidas, repetidas e faltantes, facilitando trocas sem a necessidade de portar o álbum físico.

---

## 3. Escopo

O sistema permitirá:

* Consultar todas as figurinhas do álbum;
* Marcar figurinhas obtidas;
* Registrar figurinhas repetidas;
* Consultar figurinhas faltantes;
* Consultar figurinhas repetidas;
* Visualizar estatísticas da coleção.

Não faz parte da versão 1.0:

* Login de usuário;
* Compartilhamento online;
* Integração com redes sociais;
* Troca de figurinhas pela internet.

---

## 4. Usuários do Sistema

Usuário Colecionador
Responsável por cadastrar, consultar e gerenciar sua coleção de figurinhas.

---

## 5. Requisitos Funcionais

RF01 – O sistema deve permitir visualizar todas as figurinhas do álbum.
RF02 – O sistema deve permitir marcar uma figurinha como obtida.
RF03 – O sistema deve permitir remover uma figurinha da coleção.
RF04 – O sistema deve permitir registrar a quantidade de figurinhas repetidas.
RF05 – O sistema deve permitir consultar somente as figurinhas faltantes.
RF06 – O sistema deve permitir consultar somente as figurinhas repetidas.
RF07 – O sistema deve permitir pesquisar uma figurinha pelo número.
RF08 – O sistema deve exibir estatísticas da coleção.

---

## 6. Requisitos Não Funcionais

RNF01 – O aplicativo deverá funcionar sem conexão com a internet.
RNF02 – O aplicativo deverá ser compatível com Android 8.0 ou superior.
RNF03 – O tempo de resposta para consultas deverá ser inferior a 2 segundos.
RNF04 – Os dados deverão ser armazenados localmente no dispositivo.
RNF05 – A interface deverá ser simples e intuitiva.

---

## 7. Regras de Negócio

RN01 – Uma figurinha pode existir apenas uma vez na coleção principal.
RN02 – Uma figurinha repetida deverá possuir quantidade maior que 1.
RN03 – O número de figurinhas faltantes será calculado automaticamente.
RN04 – O número de figurinhas obtidas será calculado automaticamente.
RN05 – O número de figurinhas repetidas será calculado automaticamente.

---

## 8. Critérios de Aceitação

CA01 – O usuário consegue marcar uma figurinha como obtida.
CA02 – O usuário consegue registrar uma figurinha repetida.
CA03 – O sistema exibe corretamente as figurinhas faltantes.
CA04 – O sistema exibe corretamente as figurinhas repetidas.
CA05 – O dashboard exibe estatísticas corretas da coleção.

---

## 9. Versão Inicial do Produto

A versão 1.0 será composta pelas seguintes telas:

* Dashboard
* Todas as Figurinhas
* Figurinhas Faltantes
* Figurinhas Repetidas
* Pesquisa de Figurinhas
* Configurações
