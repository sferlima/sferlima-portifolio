# SOLID

Os princípios SOLID são um conjunto de boas práticas para tornar o código mais limpo, organizado, fácil de entender e manter. Eles ajudam a evitar código desorganizado e difícil de modificar ou expandir no posteriormente.

___

## 1. Single Responsibility Principle – Princípio da Responsabilidade Única

Cada classe deve ter apenas uma responsabilidade, ou seja, cada classe deve fazer uma única coisa no sistema.
___
## 2. Open-Closed Principle – Princípio Aberto-Fechado

O código deve ser aberto para extensão, mas fechado para modificação. Podem ser adicionadas novas funcionalidades sem precisar alterar o código que já existe.
___
## 3. Liskov Substitution Principle (LSP) – Princípio da Substituição de Liskov

Você deve poder usar algo de uma classe filha (que herda algo) no lugar da classe pai (base) sem quebrar o funcionamento do programa.
___
## 4. Interface Segregation Principle (ISP) – Princípio da Segregação de Interface

Evitar criar interfaces grandes e genéricas. É melhor dividir as interfaces em partes menores e mais específicas, para que as classes implementem apenas os métodos que realmente utilizam.
___
## 5. Dependency Inversion Principle (DIP) – Princípio da Inversão de Dependência

Para o código continuar flexivel e fácil de testar as classes devem depender de abstrações (interfaces), e não de implementações concretas (classes específicas). Como por exemplo uma classe pedido não criar um metodo pagamento cartão, e sim depender de uma interface pagamento (assim poderiamos mudar o metodo de pagamento por exemplo).