1. O que entrou no escopo da v0.1

A primeira versão do Pontes Sem Gargalos tem como objetivo permitir que os usuários consultem pontes cadastradas no Recife, visualizem os principais pontos críticos de congestionamento e tenham acesso a informações sobre possíveis rotas alternativas previamente registradas.

As funcionalidades previstas para a v0.1 são:

RF01 — Listagem de pontes cadastradas

O sistema deverá apresentar uma lista das pontes disponíveis para consulta.

RF02 — Seleção de ponte

O usuário poderá selecionar uma das pontes cadastradas para consultar suas informações.

RF03 — Exibição dos pontos críticos

O sistema deverá apresentar os principais pontos de congestionamento relacionados à ponte selecionada.

RF04 — Classificação do congestionamento

Os pontos críticos deverão apresentar uma classificação de intensidade: baixo, médio ou alto.

RF05 — Localização e descrição

Cada ponto crítico deverá apresentar sua localização e uma breve descrição da situação.

RF06 — Organização das informações

As informações deverão ser apresentadas de maneira simples e organizada, facilitando a compreensão do usuário.

RF07 — Rotas alternativas cadastradas

O sistema poderá apresentar possíveis rotas alternativas, desde que estejam previamente cadastradas.

Fluxo principal de utilização

1. O usuário inicia o sistema.
2. O sistema apresenta a lista de pontes cadastradas.
3. O usuário seleciona uma ponte.
4. O sistema apresenta os pontos críticos relacionados à ponte escolhida.
5. O usuário consulta a localização, a descrição e o nível de congestionamento.
6. Caso existam alternativas cadastradas, o sistema apresenta essas opções.

Decisões de interface e organização

* A navegação deverá ser simples e intuitiva.
* As informações serão organizadas por ponte.
* Os níveis de congestionamento serão identificados como baixo, médio e alto.
* As rotas alternativas serão apresentadas somente quando existirem registros.
* Os dados utilizados na demonstração poderão ser simulados e deverão ser identificados como ilustrativos, sem representar informações de trânsito em tempo real.

⸻

2. O que ficou fora da v0.1

Para manter a primeira versão simples e compatível com o tempo e os conhecimentos técnicos da equipe, algumas funcionalidades não serão desenvolvidas neste momento.

Monitoramento em tempo real: o sistema não acompanhará o trânsito ao vivo.

Integração com GPS: não haverá identificação automática da localização do usuário.

Cálculo automático de rotas: o sistema não calculará novos caminhos nem indicará trajetos automaticamente.

Atualização automática: as informações não serão atualizadas em tempo real.

Cadastro de usuários: não será necessário criar contas ou realizar login.

Integração com aplicativos de navegação: não haverá conexão com aplicativos externos, como Google Maps ou Waze.

Previsão de congestionamentos: o sistema não utilizará inteligência artificial ou algoritmos para prever o trânsito.

Essas funcionalidades poderão ser consideradas em versões futuras, caso o projeto evolua.

⸻

3. O que fica proposto para a v0.2

Melhoria proposta: filtro por nível de congestionamento

Como possibilidade de evolução do projeto, propomos adicionar um filtro que permita ao usuário visualizar os pontos críticos de acordo com o nível de congestionamento.

Essa melhoria busca facilitar a consulta das informações, permitindo que o usuário encontre mais rapidamente os pontos classificados como baixo, médio ou alto.

A proposta deverá ser validada pela equipe e poderá ser ajustada conforme a avaliação da primeira versão.

Funcionalidades e regras propostas

RF08 — Filtro por intensidade

O sistema deverá permitir que o usuário filtre os pontos críticos de acordo com o nível de congestionamento.

RN08 — Opções de classificação

O filtro deverá apresentar as opções baixo, médio e alto.

RN09 — Exibição dos resultados

Após selecionar uma classificação, o sistema deverá apresentar somente os pontos críticos correspondentes ao nível escolhido.

RN10 — Ausência de resultados

Caso não existam pontos críticos cadastrados na classificação selecionada, o sistema deverá informar que não foram encontrados resultados.

Critérios de aceitação propostos

CA10

* Dado: que existem pontos críticos cadastrados com diferentes níveis de congestionamento.
* Quando: o usuário selecionar a opção de congestionamento alto.
* Então: o sistema deverá apresentar somente os pontos classificados como altos.
* Referência: RF08, RN08 e RN09.

CA11

* Dado: que existem pontos críticos cadastrados.
* Quando: o usuário selecionar a opção de congestionamento médio.
* Então: o sistema deverá apresentar somente os pontos classificados como médios.
* Referência: RF08, RN08 e RN09.

CA12

* Dado: que o usuário selecionar uma classificação sem pontos cadastrados.
* Quando: o sistema realizar a filtragem.
* Então: deverá informar que não foram encontrados pontos críticos para aquela classificação.
* Referência: RF08 e RN10.

CA13

* Dado: que o usuário esteja consultando os pontos críticos.
* Quando: selecionar a opção de visualizar todos os níveis.
* Então: o sistema deverá apresentar novamente todos os pontos cadastrados.
* Referência: RF08 e RN09.

⸻

4. Como registrar a verificação

Os testes abaixo foram planejados para verificar se as funcionalidades previstas para a primeira versão atendem aos critérios de aceitação.

Importante: os testes ainda não foram executados, pois a implementação do programa em Python não foi concluída. Portanto, os resultados observados permanecem pendentes e não devem ser considerados aprovados.

T01 — Listagem de pontes

* Critério relacionado: CA01.
* Entrada ou ação: iniciar o sistema e solicitar a listagem de pontes.
* Resultado esperado: o sistema deverá apresentar as pontes cadastradas.
* Resultado observado: não executado.
* Situação: pendente de execução.

T02 — Seleção de ponte

* Critério relacionado: CA02.
* Entrada ou ação: selecionar uma ponte disponível na listagem.
* Resultado esperado: o sistema deverá reconhecer a seleção e apresentar as informações correspondentes.
* Resultado observado: não executado.
* Situação: pendente de execução.

T03 — Exibição dos pontos críticos

* Critério relacionado: CA03.
* Entrada ou ação: selecionar uma ponte que possua pontos críticos cadastrados.
* Resultado esperado: o sistema deverá apresentar os pontos de congestionamento relacionados à ponte.
* Resultado observado: não executado.
* Situação: pendente de execução.

T04 — Classificação do congestionamento

* Critério relacionado: CA04.
* Entrada ou ação: consultar os pontos críticos cadastrados.
* Resultado esperado: cada ponto deverá apresentar sua classificação como baixo, médio ou alto.
* Resultado observado: não executado.
* Situação: pendente de execução.

T05 — Localização e descrição

* Critério relacionado: CA05.
* Entrada ou ação: consultar as informações de um ponto crítico.
* Resultado esperado: o sistema deverá apresentar a localização e a descrição do ponto.
* Resultado observado: não executado.
* Situação: pendente de execução.

T06 — Organização das informações

* Critério relacionado: CA06.
* Entrada ou ação: acessar as informações de uma ponte cadastrada.
* Resultado esperado: os dados deverão ser apresentados de maneira organizada e compreensível.
* Resultado observado: não executado.
* Situação: pendente de execução.

T07 — Rotas alternativas

* Critério relacionado: CA07.
* Entrada ou ação: consultar uma ponte que possua uma rota alternativa previamente cadastrada.
* Resultado esperado: o sistema deverá apresentar a alternativa registrada.
* Resultado observado: não executado.
* Situação: pendente de execução.

T08 — Opção inválida

* Critério relacionado: CA08.
* Entrada ou ação: informar uma opção inexistente no menu ou tentar selecionar uma ponte não cadastrada.
* Resultado esperado: o sistema deverá informar que a opção é inválida e permitir uma nova tentativa.
* Resultado observado: não executado.
* Situação: pendente de execução
