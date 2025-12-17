# ============================================================
# :quebra_cabeça: Problema: Agrupar Palavras por Prefixo Comum
#
# Descrição:
# Implemente um método chamado `group_by_prefix(words, n)` que agrupa
# um array de palavras pelo seu prefixo comum de comprimento `n`.
#
# Requisitos:
# - Apenas palavras com pelo menos `n` caracteres devem ser consideradas.
# - O agrupamento não deve diferenciar maiúsculas de minúsculas (ex: "Home" e "homerun" ficam juntos para n=3).
# - As formas originais das palavras devem ser preservadas na saída.
# - O resultado deve ser um array de arrays, cada subarray contendo palavras
#   com o mesmo prefixo.
#
# Exemplo:
#   group_by_prefix(["car", "cart", "cat", "bank", "banana"], 2)
#   => [["car", "cart", "cat"], ["bank", "banana"]]
#
# Restrições:
# - `words` deve ser um Array.
# - `n` deve ser um Inteiro maior que zero.
# - Elementos que não são strings devem ser ignorados.
#
# Complexidade Esperada:
#   O(k * m), onde k é o número de palavras e m é o comprimento médio das palavras.
#
# ============================================================
#
# ## O Desafio: `challenge.rb`
#
# O arquivo `challenge.rb` contém o esqueleto da solução e os testes para o problema.
# Sua tarefa é implementar o método `group_by_prefix(words, n)` na seção `TODO` do arquivo.
#
# ### Estrutura do Arquivo
#
# O arquivo `challenge.rb` inclui:
# - A seção `Implementation (TODO)` onde você deve escrever seu código.
# - Funções auxiliares de teste (`green`, `red`, `normalize`, `assert_eq`, `assert_raises`).
# - Uma suíte de testes completa para validar sua solução.
#
# ### Como Executar os Testes
#
# Para verificar sua implementação, execute o script Ruby no seu terminal:
#
# ```bash
# ruby challenge.rb
# ```
#
# Se todos os testes passarem, você verá uma mensagem de sucesso. Caso o método
# `group_by_prefix` não esteja implementado, uma `NotImplementedError` será
# lançada, e uma dica de implementação será exibida para te ajudar.
#
# ### Dica de Implementação
#
# Uma abordagem eficaz é usar um Hash para agrupar as palavras. A chave do Hash
# pode ser o prefixo em minúsculas (`word[0, n].downcase`), e o valor pode ser um
# array de palavras que compartilham esse prefixo. Itere sobre as palavras,
# valide-as de acordo com as regras (comprimento e tipo), e adicione-as ao Hash.
# No final, retorne apenas os valores do Hash.
