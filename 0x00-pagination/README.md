# README.md for 0x00 Pagination

## Introduction

Welcome to the **0x00 Pagination** project! This project provides a flexible and efficient pagination library designed to handle large datasets seamlessly. It is ideal for applications that need to present data in manageable chunks, offering an easy-to-use interface for developers.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
   - [Basic Example](#basic-example)
   - [Advanced Usage](#advanced-usage)
4. [Configuration](#configuration)
5. [API Reference](#api-reference)

## Features

- 🚀 **High Performance**: Optimized for speed and efficiency.
- 🔧 **Customizable**: Flexible configuration options to suit different needs.
- 📚 **Comprehensive Documentation**: Detailed guides and API references.
- 📦 **Lightweight**: Minimal dependencies and easy to integrate.

## Installation

To install the 0x00 Pagination library, use the following command:

```bash
npm install 0x00-pagination
```

or if you are using Yarn:

```bash
yarn add 0x00-pagination
```

## Usage

### Basic Example

Here's a simple example to get you started with 0x00 Pagination:

```javascript
const Pagination = require('0x00-pagination');

// Sample data
const data = [...Array(100).keys()]; // Array of numbers from 0 to 99

// Create a new pagination instance
const pagination = new Pagination(data, { itemsPerPage: 10 });

// Get the first page
const firstPage = pagination.getPage(1);
console.log(firstPage);
```

### Advanced Usage

For more advanced use cases, you can customize the pagination behavior:

```javascript
const Pagination = require('0x00-pagination');

// Sample data
const data = [...Array(100).keys()];

// Custom configuration
const config = {
  itemsPerPage: 5,
  currentPage: 2,
  totalPages: 20,
};

// Create a new pagination instance with custom config
const pagination = new Pagination(data, config);

// Get the second page
const secondPage = pagination.getPage(2);
console.log(secondPage);

// Get total pages
const totalPages = pagination.getTotalPages();
console.log(`Total Pages: ${totalPages}`);
```

## Configuration

The `Pagination` class accepts a configuration object with the following properties:

- `itemsPerPage` (number): Number of items per page (default: 10).
- `currentPage` (number): The current page to display (default: 1).
- `totalPages` (number): Total number of pages (optional).

## API Reference

### `Pagination`

#### Constructor

```javascript
new Pagination(data, config)
```

- `data` (Array): The dataset to paginate.
- `config` (Object): Configuration options.

#### Methods

- `getPage(pageNumber)`: Returns the items for the specified page.
- `getTotalPages()`: Returns the total number of pages.
- `setCurrentPage(pageNumber)`: Sets the current page.
- `setItemsPerPage(count)`: Sets the number of items per page.

## Contributing

We welcome contributions from the community! If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch with a descriptive name.
3. Make your changes.
4. Submit a pull request.
