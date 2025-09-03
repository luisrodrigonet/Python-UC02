# Aplicação: Inventatio

## Entidade: Ativo_Tipo

- identificacao
- descricao
- criado_em
- atualizado_em

## Entidade: Ativo

- identificacao
- nome
- descricao
- tipo_ativo #
- localizacao
- uo_responsavel #
- proprietario #
- custodiantes
- classificacao_disponibilidade
- classificacao_integridade
- classificacao_confidencilidade
- classificacao_autenticidade
- classificacao_lgpd
- valor_ativo
- status_ativo
- data_revisao
- criado_em
- atualizado_em

# Aplicacao: Riscos

## Entidade: Riscos

- Vulnerabildiade
- Ameacas
- Controle #
- impacto_confidencialidade
- impacto_integridade
- impacto_disponibilidade
- impacto_autenticidade
- impacto_privacidade
- status

## Entidade: Risco_Mapa

- risco #
- ativo #

## Entidade: Risco_Avaliacao

- 