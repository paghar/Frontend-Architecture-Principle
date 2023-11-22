### Naming Conventions

| Object Name        | Notation   | Length | Plural | Prefix | Suffix | Abbreviation | Char Mask  | Underscores |
|--------------------|------------|--------|--------|--------|--------|--------------|------------|-------------|
| Function name      | camelCase  |     50 | Yes    | No     | Yes    | Yes          | [A-z][0-9] | No          |
| Function arguments | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Local variables    | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Constants name     | PascalCase |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Field name         | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |

## Naming conventions are style guidelines for programming. They typically cover:

Always use the same naming convention for all your code. For example:
1. Do use camelCasing for variables, function names and function argument names;
2. Do use PascalCasing for global variables;
3. Do use UPPERCASE for constants (like PI);
4. Do not use under_scores in variable, constants, function arguments or function names;
5. Do not use hyphens in JavaScript names.

### Naming Conventions

Do use camelCasing for function names:

```javascript
function helloWorld()	
{
}
```

Do use camelCasing for function arguments and local variables: 

```javascript
function hello(isShow)	
{
}

firstName = "John";
lastName = "Doe";

price = 19.90;
discount = 0.10;

fullPrice = price * 100 / discount;
```

*Note: Don't start names with a $ sign. It will put you in conflict with many JavaScript library names.*

## Word Choice

✔️DO choose easily readable identifier names:

For example, a property named HorizontalAlignment is more English-readable than  AlignmentHorizontal.

✔️ DO favor readability over brevity.

The property name CanScrollHorizontally is better than ScrollableX (an obscure reference to the X-axis).

❌ DO NOT use underscores, hyphens, or any other nonalphanumeric characters.

❌ DO NOT use Hungarian notation.

❌ AVOID using identifiers that conflict with keywords of widely used programming languages.

## Using Abbreviations and Acronyms

❌ DO NOT use abbreviations or contractions as part of identifier names.

For example, use GetWindow rather than GetWin.

❌ DO NOT use any acronyms that are not widely accepted, and even if they are, only when necessary.

## Avoiding Language-Specific Names

✔️ DO use semantically interesting names rather than language-specific keywords for type names.

For example, GetLength is a better name than GetInt.

✔️ DO use a generic CLR type name, rather than a language-specific name, in the rare cases when an identifier has no semantic meaning beyond its type.