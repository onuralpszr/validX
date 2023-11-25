# ValidX  🦀 🤝 🐍

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/onuralpszr/validX/main.svg)](https://results.pre-commit.ci/latest/github/onuralpszr/validX/main)
[![CI](https://github.com/onuralpszr/validX/actions/workflows/CI.yml/badge.svg)](https://github.com/onuralpszr/validX/actions/workflows/CI.yml)

ValidX is a Python package that provides Rust-backed validators for common validation tasks. This project aims to enhance the performance of validation operations by leveraging Rust's speed ⚡️, while still being easily accessible from Python.

## 🛠 Installation

The package is not yet available on PyPI, but you can install it directly from the source:

```bash
pip install git+https://github.com/onuralpszr/validX.git
```

## 🔥 Usage

```python
>>> import validx
>>> validx.email('loremipsum@example.com')
True
>>> validx.email('loremipsum')
False
>>> validx.country_code('TR')
True
>>> validx.country_code('INVALID')
False
>>> validx.ip_address("127.0.0.1","ipv4")
True
>>> validx.ip_address("257.0.0.1","ipv4")
False
```

## 🔮 Features

ValidX provides validators of the following:

- Email Validation
- Country Code(Alpha-3, Alpha-2, Numeric) Validation

## 💻 Adding New Validators
If you want to contribute a new validator, please follow these guidelines:

* Create a new Rust module for your validator in the src directory.
* Implement the validator logic in Rust.
* Expose the validator as a Python module using the pyo3 crate.
* Update the Python package accordingly.

## Credits

This project inspired by [Validators](https://github.com/python-validators/validators)
