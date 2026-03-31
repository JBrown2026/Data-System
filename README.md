# Data System

A generic data management system demonstrating Java generics and the Repository pattern for managing Employee and Product entities.

## Overview

This project implements a reusable, type-safe `Repository<T>` class that handles common data operations such as adding, removing, and retrieving items. It showcases how to use Java generics to create flexible, maintainable code that works with different data types.

## Features

- **Generic Repository Pattern**: A reusable `Repository<T>` class that works with any data type
- **CRUD Operations**: Add, remove, retrieve, and display data
- **Type-Safe**: Leverages Java generics to ensure type safety at compile time
- **Multiple Entity Support**: Includes `Employee` and `Product` classes as examples
- **Flexible Actions**: Generic `performAction()` method that handles different entity types

## Classes

### `Repository<T>`
A generic repository class for managing collections of items.

**Methods:**
- `add(T item)` - Add an item to the repository
- `remove(T item)` - Remove an item from the repository
- `getAll()` - Retrieve all items as a copy of the list
- `findByIndex(int index)` - Find an item by its index
- `displayAll()` - Display all items in the repository
- `<U> performAction(U input)` - Perform actions on different entity types

### `Employee`
Represents an employee entity with id, name, and salary.

**Attributes:**
- `id` (int) - Employee identifier
- `name` (String) - Employee name
- `salary` (double) - Employee salary

### `Product`
Represents a product entity with id, name, and price.

**Attributes:**
- `id` (int) - Product identifier
- `name` (String) - Product name
- `price` (double) - Product price

### `Main`
The main entry point that demonstrates the usage of the Repository pattern.

## Usage Example

```java
// Create repositories for Employee and Product
Repository<Employee> empRepo = new Repository<>();
Repository<Product> prodRepo = new Repository<>();

// Add data
empRepo.add(new Employee(1, "Alice", 85000.0));
prodRepo.add(new Product(101, "Laptop", 1500.0));

// Display all items
e...