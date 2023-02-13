# YAML Cheatsheet

## Introduction

YAML (short for "YAML Ain't Markup Language") is a human-friendly data serialization standard for all programming languages. It is a popular choice for configuration files, data storage, and data exchange formats.

## Basic Syntax

- YAML uses whitespace to indicate the structure of data.
- The number of spaces before each line determines the hierarchy of data.
- Key-value pairs are separated by a colon (:)
- Strings can be wrapped in single quotes (') or double quotes (")
- Lists are indicated by a hyphen (-)
- Multiline strings are indicated by using the `|` character

## Key-Value Pairs

The basic structure of YAML consists of key-value pairs.

```yaml
key: value
```

## Lists

Lists are indicated by a hyphen (-) and are used to represent an ordered collection of items.

```yaml
- item1
- item2
- item3
```

## Multi-line Strings

Multi-line strings are indicated by using the `|` character.

```yaml
multiline_string: |
  This is line 1
  This is line 2
  This is line 3
```

## Indentation

Indentation is important in YAML, as it determines the hierarchy of data.

```yaml
parent:
  child1: value1
  child2: value2
```

## Resources

- [Official YAML Website](https://yaml.org/)
- [YAML 1.2 Specification](https://yaml.org/spec/1.2/spec.html)
- [YAML Examples](https://yaml.org/start.html)
