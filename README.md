# Blockchain-Based Cat Adoption Application

This project is a comprehensive blockchain-based cat management system, designed to streamline the process of adding, updating, deleting, and adopting cats. Developed using the Motoko programming language, this application takes advantage of the Trie data structure to efficiently manage and organize cat data in a decentralized manner.


## Libraries Used

- **Trie**: Basic Trie data structure.
- **Text**: For text processing.
- **Nat32**: For 32-bit natural numbers.
- **Bool**: Boolean (true/false) data type.
- **Option**: For optional values.

## Data Types

### `CatId`

- **Type**: `Nat32`
- **Description**: A unique identifier for a cat.

### `Cat`

- **Description**: A record containing cat information.
- **Properties**:
  - `name`: Cat's name (Type: `Text`)
  - `age`: Cat's age (Type: `Nat32`)
  - `breed`: Cat's breed (Type: `Text`)
  - `isAdopted`: Indicates if the cat is adopted (Type: `Bool`)

### `ResponseCat`

- **Description**: The response structure for cat information.
- **Properties**:
  - `name`: Cat's name (Type: `Text`)
  - `age`: Cat's age (Type: `Nat32`)
  - `breed`: Cat's breed (Type: `Text`)
  - `isAdopted`: Indicates if the cat is adopted (Type: `Bool`)
  - `id`: Cat's unique identifier (Type: `Nat32`)

## Functions

### `addCat`

- **Description**: Adds a new cat.
- **Input**: 
  - `cat`: The cat to be added (Type: `Cat`)
- **Output**: 
  - `Text`: Message indicating the result of the operation (`"Cat Added Successfully"`)

### `updateCat`

- **Description**: Updates an existing cat.
- **Input**: 
  - `catId`: The ID of the cat to be updated (Type: `CatId`)
  - `cat`: Updated cat information (Type: `Cat`)
- **Output**: 
  - `Bool`: Value indicating whether the update was successful

### `deleteCat`

- **Description**: Deletes an existing cat.
- **Input**: 
  - `catId`: The ID of the cat to be deleted (Type: `CatId`)
- **Output**: 
  - `Bool`: Value indicating whether the deletion was successful

### `adoptCat`

- **Description**: Marks an existing cat as adopted.
- **Input**: 
  - `catId`: The ID of the cat to be adopted (Type: `CatId`)
- **Output**: 
  - `Bool`: Value indicating whether the adoption was successful

### `key`

- **Description**: Converts a `CatId` to a Trie key.
- **Input**: 
  - `x`: The cat's ID (Type: `CatId`)
- **Output**: 
  - `Trie.Key<CatId>`: Trie key

## Project Setup and Execution

1. Download and open the project files.
2. Install the required dependencies.
3. Compile and run the project.

## Example Usage

Below are examples demonstrating how to use the functionalities provided by this project:

### Adding a Cat

```motoko
let cat = {name = "Whiskers"; age = 2; breed = "Siamese"; isAdopted = false};
let result = await addCat(cat); 
 ```
### Updating a Cat

```motoko
let cat = {name = "Whiskers"; age = 3; breed = "Siamese"; isAdopted = false};
let updateResult = await updateCat(0, cat); // Assuming the CatId is 0
 ```
### Deleting a Cat

```motoko
let deleteResult = await deleteCat(0); // Assuming the CatId is 0
 ```
### Adopting a Cat

```motoko
let adoptResult = await adoptCat(0); // Assuming the CatId is 0
 ```

## Contribution

The Blockchain-Based-Cat-Adoption-Application represents a powerful, decentralized solution for managing cat data, incorporating advanced programming techniques and modern blockchain technology. This application serves as an exemplar of how secure, efficient, and transparent processes can be implemented in practical applications, fostering trust and operational efficiency in pet adoption services.

