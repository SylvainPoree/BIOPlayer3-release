# Principais alterações

- UI: Melhor identificação da música em reprodução (nota musical) na sessão e nos resultados de pesquisa.
- UI: Melhorado o aspeto visual do controlador.
- UI: Removido o código restante da bola de carregamento oscilante no ecrã Fusion.
- DEBUG: Corrigidas áreas invisíveis que podiam intercetar cliques no ecrã inicial: agora é possível clicar nas bandeiras e nos botões mesmo quando Kiki ou -BIOPlayer- estão por cima.
- FUNCIONALIDADE: Melhorada a recuperação do identificador: uma chave de licença em falta é gerada automaticamente se a conta ainda utilizava o valor temporário `000-000-000`.
- TECH: Melhorada a publicação das notas de atualização no GitHub Pages, sem dependência de `rsync`.
- TECH: Separação dos instaladores Windows por canal: `BIOPlayer`, `BIOPlayer Beta` e `BIOPlayer Dev` podem agora coexistir no mesmo computador.
- UI: Corrigido o campo editor do Windows: permanece `BIOPlayer` para todos os canais.
