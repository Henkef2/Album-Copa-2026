                    +----------------------+
                    |  Álbum Digital Copa  |
                    +----------------------+

      Colecionador
      |
      |------------------> (Consultar Coleção)
      | UC01 - Consultar Coleção
      |------------------> (Marcar Figurinha Obtida)
      | UC02 - Marcar Figurinha Obtida
      |------------------> (Registrar Figurinha Repetida)
      | UC03 - Registrar Figurinha Repetida
      |------------------> (Consultar Faltantes)
      | UC04 - Consultar Faltantes
      |------------------> (Consultar Repetidas)
      | UC05 - Consultar Repetidas
      |------------------> (Pesquisar Figurinha)
      | UC06 - Pesquisar Figurinha
      |------------------> (Visualizar Estatísticas)
      | UC07 - Visualizar Estatísticas

------------------
      | UC01 - Consultar Coleção
      Objetivo
      Permitir visualizar todas as figurinhas do álbum.
      
      Ator
      Colecionador
      
      Fluxo Principal
      1-Usuário acessa a tela de coleção.
      2-Sistema exibe todas as figurinhas.
      3-Sistema mostra as figurinha obtidas coloridas e as não obtidas preto/branco.
      4-Sistema exibe a numeração de todas as figurinhas
      
      Resultado
      Coleção completa exibida com sucesso.
------------------      
      | UC02 - Marcar Figurinha Obtida
      Objetivo
      Registrar que o usuário possui determinada figurinha.
      
      Fluxo
      1-Usuário visualiza o album com todas as figurinha.
      2-Seleciona uma figurinha e marca como obtida.
      3-Sistema atualiza o banco de dados.
      4-Estatísticas são recalculadas.

      Resultado
      As figurinhas obtidas aparecerão coloridas, as figurinhas não obtidas aparecerão em preto/branco
------------------      
      | UC03 - Registrar Figurinha Repetida
      Objetivo
      Controlar figurinhas repetidas.
      
      Fluxo
      1-Usuário seleciona uma figurinha colorida (já obtida).
      2-Informa quantidade de figurinhas repetidas que possui.
      3-Sistema mostra a quantidade de figurinhas, por ex: x3 (possui 3 figurinhas)
      3-Sistema salva quantidade.
------------------      
      | UC04 - Consultar Faltantes
      Objetivo
      Exibir figurinhas não obtidas.
      
      Fluxo
      1-Usuário visualiza todas as figurinhas coloridas (obtidas) e preto/branco (Faltantes).
      2-Disponibilizar filtro de seleção apenas faltantes, que oculta as figurinhas obtidas.
      3-Exibe apenas faltantes.
------------------      
      | UC05 - Consultar Repetidas
      Objetivo
      Exibir apenas figurinhas repetidas.
      
      Fluxo
      1-Usuário seleciona filtro "Repetidas".
      2-Sistema filtra a coleção e oculta as figurinhas obtidas que não há repetição.
      3-Exibe quantidade de cada figurinha repetida.
------------------      
      | UC06 - Pesquisar Figurinha
      Objetivo
      Localizar figurinha pelo número.
      
      Fluxo
      1-Usuário informa número.
      2-Sistema realiza busca.
      3-Sistema exibe resultado.
------------------      
      | UC07 - Visualizar Estatísticas
      Objetivo
      Exibir progresso da coleção.
      
      Fluxo
      1-Usuário acessa Dashboard.
      2-Sistema calcula:
        2.1-Obtidas
        2.2-Faltantes
        2.3-Repetidas
      3-Sistema exibe resumo.

------------------
