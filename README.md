# Desafio: produtos
Você precisa fazer um CRUD de produtos de uma loja. Simples, certo? Mas precisa ser feito direito!

# Requisitos de negócio
Precisa permitir a criação, alteração, deleção e busca de produtos.
- A criação e alteração só podem ser feitas por usuários com a role `backoffice`
- A deleção só pode ser feita com a role `admin`
- A busca deve:
    - ser pública (pode acessar sem estar autenticado ou autorizado)
    - permitir busca geral de produtos sem filtros apenas com o id, nome e preço
    - permitir detalhamento do produto por ID (trazer todos os campos do banco)

# Requisitos funcionais
- Toda a solução deve respeitar o padrão REST, respeitando todos os códigos HTTP
- Deve existir a validação dos campos nome (não pode ser vazio), e preço (não pode ser menor ou igual a zero). Não use o anti pattern `arrow` para validação dos dados.
- Os ids devem ser GUIDs gerados por timestamp 
- A busca por produtos deve ser paginada (apenas X produtos por vez)
- A solução deve ter um cache para produtos mais buscados (pode ser o que você mais gostar)
- A solução deve ser separada em microserviços (microserviços de autenticação, microserviço de autorização, microserviço de produtos)
- A integração entre os microserviços de produtos com autenticação e microserviços com autorização deve ser síncrono
- Os 3 microserviços devem ser escaláveis horizontalmente
- Cada microserviços deve ter um dockerfile próprio e um repositório próprio
- O desenvolvimento não pode ser feito na master, é necessário criar uma branch `develop` separada da master
- Os microserviços devem ser gerenciados por um kubernetes


# Próximos passos
- Inclusão de imagem nos produtos
- Separação das bases de escrita e leitura
- Sincronização de bases asíncronamente
- Busca textual por score
- ...
