# Arquitetura MVVM

## Objetivo

O aplicativo Álbum Digital Copa 2026 utilizará a arquitetura MVVM (Model-View-ViewModel) para separar responsabilidades, facilitar manutenção, testes e evolução do sistema.

---

## Estrutura da Arquitetura

Usuário
↓
MainScreen / DetailScreen
↓
StickerViewModel
↓
StickerRepository
↓
StickerDao
↓
Room Database

---

## Camada View

Responsável pela interface gráfica apresentada ao usuário.

### Componentes

* MainScreen
* DetailScreen

### Responsabilidades

* Exibir figurinhas
* Exibir estatísticas
* Exibir filtros
* Receber cliques do usuário

---

## Camada ViewModel

Responsável por controlar o estado da interface.

### Componente

* StickerViewModel

### Responsabilidades

* Carregar figurinhas
* Atualizar quantidades
* Aplicar filtros
* Calcular estatísticas
* Atualizar a interface

---

## Camada Repository

Responsável pela comunicação entre ViewModel e Banco de Dados.

### Componente

* StickerRepository

### Responsabilidades

* Consultar figurinhas
* Salvar alterações
* Centralizar acesso aos dados

---

## Camada DAO

Responsável pelas consultas ao banco.

### Componente

* StickerDao

### Responsabilidades

* Buscar figurinhas
* Inserir registros
* Atualizar quantidades
* Filtrar faltantes
* Filtrar repetidas

---

## Camada Database

Responsável pelo armazenamento persistente.

### Componente

* StickerDatabase

### Tecnologia

* Room Database

### Responsabilidades

* Armazenar figurinhas
* Persistir alterações
* Disponibilizar dados para o DAO

---

## Benefícios

* Código organizado
* Facilidade de manutenção
* Facilidade para testes
* Separação de responsabilidades
* Arquitetura recomendada pela Google


obs: mapa do APP

app/

├── data/
│   ├── Sticker.kt
│   ├── StickerDao.kt
│   └── StickerDatabase.kt
│
├── repository/
│   └── StickerRepository.kt
│
├── viewmodel/
│   └── StickerViewModel.kt
│
├── ui/
│   ├── MainScreen.kt
│   └── DetailScreen.kt
