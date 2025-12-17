# 🧩 Agrupar Palavras por Prefixo Comum

## 📌 Descrição

Implemente um método chamado `group_by_prefix(words, n)` que agrupa um array de palavras pelo seu prefixo comum de comprimento **`n`**.

---

## ✅ Requisitos

* Apenas palavras com **pelo menos `n` caracteres** devem ser consideradas
* O agrupamento **não deve diferenciar maiúsculas de minúsculas**
  (ex.: `"Home"` e `"homerun"` ficam juntos para `n = 3`)
* As **formas originais das palavras** devem ser preservadas na saída
* O resultado deve ser um **array de arrays**, onde cada subarray contém palavras com o mesmo prefixo

---

## 🧪 Exemplo

```ruby
group_by_prefix(["car", "cart", "cat", "bank", "banana"], 2)
# => [["car", "cart", "cat"], ["bank", "banana"]]
```

---

## ⚠️ Restrições

* `words` deve ser um **Array**
* `n` deve ser um **Inteiro maior que zero**
* Elementos que **não forem strings** devem ser ignorados

---

## ⏱️ Complexidade Esperada

```
O(k * m)
```

Onde:

* `k` é o número de palavras
* `m` é o comprimento médio das palavras

---

## 🧠 O Desafio: `challenge.rb`

O arquivo **`challenge.rb`** contém o esqueleto da solução e os testes do problema.

Sua tarefa é implementar o método:

```ruby
group_by_prefix(words, n)
```

na seção **`TODO`** do arquivo.

---

## 🗂️ Estrutura do Arquivo

O arquivo `challenge.rb` inclui:

* ✍️ A seção **Implementation (TODO)** para escrever sua solução
* 🧪 Funções auxiliares de teste:

  * `green`
  * `red`
  * `normalize`
  * `assert_eq`
  * `assert_raises`
* ✅ Uma suíte de testes completa para validar sua implementação

---

## ▶️ Como Executar os Testes

No terminal, execute:

```bash
ruby challenge.rb
```

### Resultado esperado

* ✔️ Se todos os testes passarem, uma mensagem de sucesso será exibida
* ❌ Se o método `group_by_prefix` não estiver implementado, uma `NotImplementedError` será lançada com uma dica de implementação

---

## 💡 Dica de Implementação

Uma abordagem eficaz é usar um **Hash** para agrupar as palavras:

* **Chave**: prefixo em minúsculas

```ruby
word[0, n].downcase
```

* **Valor**: array de palavras que compartilham o mesmo prefixo

### Passos sugeridos:

1. Itere sobre as palavras
2. Valide:

   * tipo (`String`)
   * comprimento mínimo (`n`)
3. Agrupe no Hash
4. Retorne apenas os valores do Hash
