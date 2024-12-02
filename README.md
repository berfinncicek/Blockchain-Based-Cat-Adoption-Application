# Blockchain-Based-Cat-Adoption-Application

This project includes a simple blockchain-based cat management system that allows adding, updating, deleting, and adopting cats. The project is developed using the Motoko programming language and utilizes the Trie data structure.

## Libraries Used
- **Trie**: Basic Trie data structure.
- **Text**: For text processing.
- **Nat32**: For 32-bit natural numbers.
- **Bool**: Boolean (true/false) data type.
- **Option**: For optional values.

## Data Types
- **CatId**: A unique cat identifier of type `Nat32`.
- **Cat**: A record containing cat information:
  - `name`: Cat's name (`Text`).
  - `age`: Cat's age (`Nat32`).
  - `breed`: Cat's breed (`Text`).
  - `isAdopted`: Indicates if the cat is adopted (`Bool`).
- **ResponseCat**: The response structure for cat information:
  - `name`: Cat's name (`Text`).
  - `age`: Cat's age (`Nat32`).
  - `breed`: Cat's breed (`Text`).
  - `isAdopted`: Indicates if the cat is adopted (`Bool`).
  - `id`: Cat's unique identifier (`Nat32`).
