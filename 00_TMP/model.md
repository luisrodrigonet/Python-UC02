# Aplicação: Inventatio

## Entidade: Ativo_Tipo

- identificacao
- descricao
- criado_em
- atualizado_em

## Entidade: Ativo

- tipo_ativo #
- identificacao
- descricao
- proprietario
- custodiantes
- valor_ativo
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