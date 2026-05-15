# Funcionalidade adicional: Histórico de reservas por usuário

  ## Objetivo
  Permitir consultar todas as reservas associadas a um usuário, incluindo
  reservas confirmadas e canceladas.

  ## Padrão adicional usado
  Chain of Responsibility.

  ## Justificativa
  O sistema já possui validações de criação de reserva dentro de `ProxyReserva`,
  mas elas ficam concentradas em uma única classe. A Chain of Responsibility
  separa cada validação em um handler próprio, permitindo adicionar, remover ou
  reorganizar regras sem alterar a lógica principal de criação de reservas.

  ## Como testar
  1. Cadastrar uma sala.
  2. Cadastrar um usuário.
  3. Criar reservas para esse usuário.
  4. Cancelar ou modificar alguma reserva.
  5. Acessar a opção de histórico por usuário.