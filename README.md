# Projeto-API
# API utilizada:
Decidi utilizar a API pública e gratuita *Disney API*, disponível em *https://disneyapi.dev*. Essa API é mantida pela comunidade, não exige autenticação e possui mais de 9.800 personagens da Disney, incluindo filtro de busca nativo por nome.

# O que é desenvolvido:
O projeto permite pesquisar apenas as **princesas oficiais da linha Disney Princess**. A lista de princesas (nome, filme, ano, reino e descrição) foi traduzida e cadastrada manualmente em português, já que a API retorna essas informações apenas em inglês. A única informação buscada em tempo real na API é a **imagem oficial** de cada princesa, retornada no campo `imageUrl`.

Princesas disponíveis para pesquisa:
*Branca de Neve, Cinderela, Aurora, Ariel, Bela, Jasmine, Pocahontas, Mulan, Tiana, Rapunzel, Merida, Moana e Raya*

# Endereço chamado:
A imagem de cada princesa é buscada através do endpoint de filtro por nome...
*https://api.disneyapi.dev/character?name=NOME_EM_INGLES*

Exemplo de chamada real feita pelo sistema ao pesquisar "Ariel":
*https://api.disneyapi.dev/character?name=Ariel*

# Como rodar:
Na aba de pesquisa, digite o nome de uma princesa (o campo sugere os nomes automaticamente) e clique em "Pesquisar", ou pressione Enter. As informações aparecerão em português, junto com a imagem oficial da personagem.

# Captura do sistema funcionando:
*Ariel*
![alt text](image-1.png)

*Moana*
![alt text](image-2.png)

# Dificuldade encontrada:
O principal desafio foi que a API retorna todos os dados (nomes de filmes, séries, aparições) apenas em inglês, sem opção de tradução. Como o objetivo era exibir as informações em português, optamos por manter uma base de dados local apenas para os textos (filme, ano, reino, descrição), usando a API somente para trazer a imagem oficial de cada princesa. Também foi necessário restringir manualmente a busca a uma lista fixa de princesas, já que a API original permite buscar qualquer personagem Disney, não apenas princesas.
