# JAVA COLLECTIONS

| Tipo         | Interface     | Permite Duplicatas | Ordenação               | Exemplo de Implementação       | Performance (Acesso) | Performance (Inserção/Remoção) | Principais Métodos                         |
|--------------|---------------|---------------------|-------------------------|--------------------------------|----------------------|----------------------------------|--------------------------------------------|
| **Collection** | -             | Sim/Não              | Não                     | -                              | -                    | -                                | `add()`, `remove()`, `size()`, `clear()` |
| **List**     | `Collection`  | Sim                 | Sim                     | `ArrayList`, `LinkedList`, `Vector` | Rápido (`ArrayList`) | Lento (`ArrayList`), Rápido (`LinkedList`) | `get()`, `set()`, `add()`, `remove()`, `indexOf()` |
| **Set**      | `Collection`  | Não                 | Sim (com `TreeSet`)    | `HashSet`, `LinkedHashSet`, `TreeSet` | Rápido (`HashSet`)  | Rápido (`LinkedHashSet`)         | `add()`, `remove()`, `contains()`, `size()` |
| **Map**      | `Collection`  | Não (chaves)       | Sim (com `TreeMap`)    | `HashMap`, `LinkedHashMap`, `TreeMap` | Rápido (`HashMap`)  | Rápido (`LinkedHashMap`)         | `put()`, `get()`, `remove()`, `keySet()`, `values()` |

## Notas

- **Collection**: Interface base para todas as coleções.
- **List**: Mantém a ordem dos elementos e permite duplicatas.
- **Set**: Não permite duplicatas e não garante a ordem dos elementos (exceto `LinkedHashSet` e `TreeSet`).
- **Map**: Armazena pares chave-valor, onde as chaves são únicas.
