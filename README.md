# FormBuilder

## Overview

FormBuilder is a PHP library designed to simplify the creation and management of HTML forms. It provides a fluent interface for building forms with various input types, methods, and attributes, making it easier to integrate form functionality into your PHP applications.

## Features

- Supports multiple form methods: GET, POST, PUT, DELETE, PATCH.
- Easily add various input types, including text, password, checkbox, radio, and more.
- Create text areas, buttons, and select fields with customizable options.
- Fluent interface for chaining method calls.
- Simple attribute management for form elements.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/skonile/FormBuilder.git
   ```
2. Navigate to the project directory:
   ```bash
   cd FormBuilder
   ```
3. Include the FormBuilder library in your PHP project:
   ```php
   require_once 'path/to/FormBuilder.php';
   ```

## Usage

Here's a basic example of how to use the FormBuilder library:

```php
use App\FormBuilder\FormBuilder;
use App\FormBuilder\FormMethod;
use App\FormBuilder\InputType;

$form = new FormBuilder();
$form->setMethod(FormMethod::POST)
     ->setAction('/submit-form')
     ->addInput('username', InputType::TEXT, ['placeholder' => 'Enter your username'])
     ->addInput('password', InputType::PASSWORD, ['placeholder' => 'Enter your password'])
     ->addButton('submit', 'Submit', ['class' => 'btn btn-primary']);

echo $form->getForm();
```

## Configuration

- Customize form attributes by passing an associative array to the `FormBuilder` constructor.
- Use the `addAttributes` method to add custom attributes to form elements.

## License

This project is licensed under the Apache 2.0.

## Contact

For questions or support, please contact [siyabongakonile@gmail.com].
