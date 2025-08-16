# 📘 Documentação: Laço de repetição `for` no JavaScript

## 🔹 O que é um laço de repetição?

Um **laço de repetição (loop)** é uma estrutura que permite executar um bloco de código várias vezes, de forma automática, sem que seja necessário escrever o mesmo código repetidamente.

No JavaScript, temos diferentes tipos de loops (`for`, `while`, `do...while`, etc.), mas o **mais comum e usado é o `for`**.

---

## 🔹 Estrutura do `for`

A sintaxe do `for` é a seguinte:

```javascript
for (inicialização; condição; incremento) {
  // bloco de código que será repetido
}
```

### ✅ Explicando cada parte:

1. **Inicialização** → Geralmente usada para declarar e iniciar uma variável de controle (ex: `let i = 0`).
2. **Condição** → Enquanto for verdadeira, o loop continua executando (ex: `i < 5`).
3. **Incremento** → Atualiza o valor da variável de controle a cada repetição (ex: `i++`).

---

## 🔹 Exemplo básico

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Número: " + i);
}
```

### 🛠️ Como funciona:

1. `let i = 0` → a variável começa em 0.
2. `i < 5` → enquanto `i` for menor que 5, o código dentro do `{ }` será executado.
3. `i++` → a cada volta do loop, soma +1 em `i`.

**Saída no console:**

```
Número: 0
Número: 1
Número: 2
Número: 3
Número: 4
```

---

## 🔹 Fluxo de execução

1. A **inicialização** é executada apenas **uma vez**.
2. A **condição** é testada. Se for `true`, executa o bloco.
3. Depois executa o **incremento**.
4. Volta para a **condição** e repete.
5. Quando a **condição for falsa**, o loop para.

---

## 🔹 Exemplos práticos

### 📌 Contando de 1 até 10

```javascript
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

---

### 📌 Contando de 10 até 1 (decrescente)

```javascript
for (let i = 10; i >= 1; i--) {
  console.log(i);
}
```

---

### 📌 Trabalhando com arrays

O `for` é muito usado para percorrer listas de dados:

```javascript
let frutas = ["Maçã", "Banana", "Laranja", "Uva"];

for (let i = 0; i < frutas.length; i++) {
  console.log("Fruta: " + frutas[i]);
}
```

**Saída:**

```
Fruta: Maçã
Fruta: Banana
Fruta: Laranja
Fruta: Uva
```

---

### 📌 Pulando repetições com `continue`

```javascript
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    continue; // pula o número 3
  }
  console.log(i);
}
```

**Saída:**

```
1
2
4
5
```

---

### 📌 Interrompendo o loop com `break`

```javascript
for (let i = 1; i <= 5; i++) {
  if (i === 4) {
    break; // para o loop quando chegar em 4
  }
  console.log(i);
}
```

**Saída:**

```
1
2
3
```

---

## 🔹 Dicas importantes

✔️ Use o `for` quando souber exatamente **quantas vezes** precisa repetir algo.
✔️ Prefira `while` quando a repetição depender de uma condição mais aberta.
✔️ Cuidado com loops infinitos (quando a condição nunca fica falsa).

Exemplo de loop **infinito** (não faça isso 😅):

```javascript
for (let i = 0; i >= 0; i++) {
  console.log(i); // nunca vai parar!
}
```

---

## 🔹 Resumindo

* O `for` é um loop controlado por **contador**.
* Estrutura: `for (inicialização; condição; incremento) { }`
* Ideal para **contagens** e para percorrer **arrays**.
* Pode usar `break` para parar e `continue` para pular uma volta do loop.

