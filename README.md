# Алгоритми для AVL-дерев

Цей репозиторій містить домашню роботу з реалізації різних алгоритмів для роботи з AVL-деревами.

## Функції

### Знаходження найбільшого значення

Функція `find_maximum` знаходить найбільше значення в AVL-дереві, проходячи від кореня до самого правого вузла.

```python
def find_maximum(root):
    if root is None:
        return None
    current = root
    while current.right is not None:
        current = current.right
    return current.key

### Знаходження найменшого значення

Функція find_minimum знаходить найменше значення в AVL-дереві, проходячи від кореня до самого лівого вузла.

def find_minimum(root):
    if root is None:
        return None
    current = root
    while current.left is not None:
        current = current.left
    return current.key

### Знаходження суми всіх значень

Функція find_sum знаходить суму всіх значень у AVL-дереві, рекурсивно обходячи дерево та підсумовуючи всі ключі.

def find_sum(root):
    if root is None:
        return 0
    return root.key + find_sum(root.left) + find_sum(root.right)
