# Plano Técnico Full-Stack para Revisão e Expansão do Site do Grupo de Pesquisa

## Objetivo

Este documento apresenta um plano técnico para revisão, melhoria e expansão do site de um grupo de pesquisa, considerando responsabilidades de desenvolvimento **front-end**, **back-end**, estrutura de dados, segurança, SEO, acessibilidade, testes, publicação e manutenção.

O objetivo é garantir que o site seja institucionalmente sólido, tecnicamente sustentável, fácil de atualizar e adequado para divulgar equipe, projetos, publicações, notícias, eventos e materiais do grupo.

---

## 1. Levantamento inicial do projeto

Antes de iniciar alterações, o desenvolvedor deve compreender a base técnica atual do site.

### Itens a verificar

| Item | O que avaliar |
|---|---|
| Tecnologia atual | WordPress, React, Next.js, HTML/CSS, Wix, Webflow, Django, Laravel etc. |
| Hospedagem | Servidor próprio, Vercel, Netlify, Hostinger, servidor institucional, AWS etc. |
| Domínio | Configuração de DNS, HTTPS e redirecionamentos |
| CMS | Existência de painel para editar conteúdos |
| Banco de dados | Estrutura, entidades e relacionamentos |
| Repositório | GitHub, GitLab ou outro sistema de versionamento |
| Responsividade | Funcionamento em celular, tablet e desktop |
| Performance | Velocidade de carregamento e otimização |
| Segurança | Login, permissões, backups e atualizações |
| SEO | Títulos, descrições, URLs amigáveis e indexação |

### Entregável

- Relatório inicial com diagnóstico técnico do site.
- Lista de riscos e problemas prioritários.
- Mapeamento das funcionalidades existentes e ausentes.

---

## 2. Auditoria técnica

A auditoria deve cobrir tanto o front-end quanto o back-end.

---

## 2.1 Auditoria de front-end

### Pontos de revisão

- Layout geral.
- Menu e navegação.
- Hierarquia visual das páginas.
- Responsividade.
- Acessibilidade.
- Padronização de fontes, cores, botões e espaçamentos.
- Componentes reutilizáveis.
- Compatibilidade com navegadores.
- Estados de carregamento e erro.
- Otimização de imagens.
- Links quebrados.
- Estrutura para português e possível versão em inglês.
- Clareza das chamadas na página inicial.
- Consistência visual entre páginas.

### Entregável

- Relatório de problemas visuais, técnicos e de usabilidade.
- Lista de ajustes de front-end por prioridade.

---

## 2.2 Auditoria de back-end

### Pontos de revisão

- Estrutura do banco de dados.
- APIs existentes.
- Sistema de login.
- Painel administrativo.
- Permissões de usuário.
- Upload de imagens e arquivos.
- Formulário de contato.
- Integrações externas.
- Segurança das rotas.
- Validação de dados.
- Backups.
- Logs de erro.
- Dependências e atualizações.

### Entregável

- Relatório técnico da arquitetura atual.
- Identificação de riscos de segurança.
- Lista de melhorias necessárias no back-end.

---

## 3. Arquitetura recomendada

Para um site de grupo de pesquisa, recomenda-se uma arquitetura que permita atualização de conteúdo sem depender continuamente do desenvolvedor.

### Opções possíveis

| Solução | Quando usar |
|---|---|
| WordPress | Quando a prioridade for facilidade editorial |
| Next.js + CMS | Quando se deseja um site moderno, rápido e personalizado |
| Astro + CMS | Quando se deseja um site institucional leve e performático |
| React + API própria | Quando há necessidade de alta personalização |
| Django | Quando a equipe já utiliza Python e quer um back-end robusto |
| Strapi | Quando se deseja CMS headless com API |
| Directus | Quando se deseja CMS conectado diretamente ao banco |
| Sanity | Quando se deseja CMS online, flexível e colaborativo |
| Supabase | Quando se deseja banco, autenticação e storage integrados |
| Firebase | Quando se deseja simplicidade e infraestrutura gerenciada |

### Recomendação geral

Para um grupo de pesquisa acadêmico, há três caminhos principais:

1. **Opção simples:** WordPress bem configurado.
2. **Opção moderna:** Next.js + CMS headless.
3. **Opção leve:** Astro + CMS headless.

A escolha depende do nível de autonomia editorial desejado, da equipe técnica disponível e da necessidade de personalização.

---

## 4. Modelagem de dados

O back-end deve organizar o conteúdo em entidades claras e fáceis de manter.

---

## 4.1 Entidade: Integrante

### Campos sugeridos

- Nome.
- Foto.
- Categoria.
- Mini bio.
- E-mail.
- Instituição.
- Cargo ou vínculo.
- Linhas de pesquisa.
- Link para Lattes.
- Link para ORCID.
- Link para Google Scholar.
- Página pessoal.
- Ordem de exibição.
- Status: ativo, egresso ou colaborador.

### Categorias possíveis

- Coordenação.
- Pesquisadores.
- Pós-doutorandos.
- Doutorandos.
- Mestrandos.
- Graduandos.
- Iniciação científica.
- Egressos.
- Colaboradores externos.

---

## 4.2 Entidade: Projeto

### Campos sugeridos

- Título.
- Resumo.
- Descrição completa.
- Coordenador.
- Equipe.
- Financiamento.
- Agência de fomento.
- Período.
- Status.
- Linha de pesquisa.
- Imagem.
- Publicações relacionadas.
- Link externo.

### Status possíveis

- Em andamento.
- Concluído.
- Suspenso.
- Em planejamento.

---

## 4.3 Entidade: Publicação

### Campos sugeridos

- Título.
- Autores.
- Ano.
- Tipo.
- Revista, editora ou evento.
- DOI.
- Link externo.
- Arquivo PDF, se permitido.
- Projeto relacionado.
- Linha de pesquisa.
- Destaque na página inicial.

### Tipos possíveis

- Artigo.
- Livro.
- Capítulo.
- Trabalho em anais.
- Relatório técnico.
- Texto de divulgação científica.
- Produto técnico.
- Dataset.
- Software.

---

## 4.4 Entidade: Notícia

### Campos sugeridos

- Título.
- Resumo.
- Texto completo.
- Imagem de capa.
- Data.
- Autor.
- Categoria.
- Tags.
- Slug/URL.
- Status: rascunho ou publicado.

### Categorias possíveis

- Publicação.
- Evento.
- Projeto.
- Chamada.
- Defesa.
- Prêmio.
- Parceria.
- Divulgação científica.

---

## 4.5 Entidade: Evento

### Campos sugeridos

- Título.
- Data.
- Horário.
- Local ou link.
- Descrição.
- Link de inscrição.
- Imagem.
- Organização.
- Status: próximo ou realizado.

---

## 4.6 Entidade: Linha de pesquisa

### Campos sugeridos

- Nome.
- Descrição.
- Pesquisadores vinculados.
- Projetos vinculados.
- Publicações vinculadas.
- Ordem de exibição.

---

## 4.7 Entidade: Material ou Recurso

### Campos sugeridos

- Título.
- Descrição.
- Tipo de material.
- Arquivo.
- Link externo.
- Autores.
- Ano.
- Projeto relacionado.
- Licença de uso.
- Tags.

### Tipos possíveis

- Relatório.
- Guia.
- Dataset.
- Apresentação.
- Vídeo.
- Boletim.
- Protocolo de pesquisa.
- Material didático.

---

## 5. Desenvolvimento front-end

O front-end deve ser claro, responsivo, acessível e coerente com a identidade acadêmica do grupo.

---

## 5.1 Páginas principais

| Página | Função |
|---|---|
| Início | Apresentação, destaques e chamadas principais |
| Sobre | História, missão, objetivos e vínculos institucionais |
| Equipe | Listagem filtrável dos integrantes |
| Integrante individual | Perfil completo de cada pesquisador |
| Linhas de pesquisa | Organização temática do grupo |
| Projetos | Projetos em andamento e concluídos |
| Projeto individual | Página detalhada do projeto |
| Publicações | Produção científica com filtros |
| Notícias | Atualizações do grupo |
| Notícia individual | Página de notícia completa |
| Eventos | Agenda e histórico |
| Materiais | Downloads, relatórios, datasets e guias |
| Parcerias | Instituições e redes |
| Contato | Formulário, e-mail e localização |

---

## 5.2 Componentes reutilizáveis

O desenvolvedor deve criar componentes reutilizáveis para facilitar manutenção e expansão.

### Componentes sugeridos

- Card de integrante.
- Card de projeto.
- Card de publicação.
- Card de notícia.
- Card de evento.
- Banner principal.
- Lista de destaques.
- Filtros por ano, tema e categoria.
- Botões padronizados.
- Breadcrumbs.
- Paginação.
- Campo de busca.
- Componente de DOI/link externo.
- Componente de logos de parceiros.
- Componente de chamada para contato.
- Componente de rodapé institucional.

---

## 5.3 Funcionalidades front-end

### Funcionalidades prioritárias

- Menu responsivo.
- Busca interna.
- Filtros em publicações.
- Filtros em projetos.
- Filtros na equipe por categoria.
- Página individual para projetos.
- Página individual para notícias.
- Compartilhamento social.
- Formulário de contato com validação.
- Layout otimizado para celular.

### Funcionalidades opcionais

- Modo multilíngue.
- Newsletter.
- Área de vídeos.
- Página de imprensa.
- Galeria.
- Repositório de dados.
- Integração com calendário de eventos.

---

## 6. Desenvolvimento back-end

O back-end deve permitir que o grupo atualize conteúdos sem alterar código.

---

## 6.1 Painel administrativo

### Funcionalidades necessárias

- Login seguro.
- Perfis de usuário.
- Editor de notícias.
- Cadastro de integrantes.
- Cadastro de projetos.
- Cadastro de publicações.
- Upload de imagens.
- Upload de arquivos.
- Cadastro de eventos.
- Cadastro de materiais.
- Rascunho e publicação.
- Ordenação manual de destaques.
- Controle de permissões.

### Perfis de usuário sugeridos

| Perfil | Permissões |
|---|---|
| Administrador | Acesso total |
| Editor | Criar e editar conteúdos |
| Autor | Criar conteúdos, mas não publicar |
| Leitor interno | Visualizar conteúdos restritos, se houver |

---

## 6.2 APIs e rotas

O back-end deve disponibilizar endpoints ou consultas para alimentar o front-end.

### Exemplos de rotas

```
GET /api/members
GET /api/members/:slug
GET /api/projects
GET /api/projects/:slug
GET /api/publications
GET /api/news
GET /api/news/:slug
GET /api/events
GET /api/materials
POST /api/contact
```
