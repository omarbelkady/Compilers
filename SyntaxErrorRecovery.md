# Syntax Error Recovery

## Theory
Error recovery strategies ensure parsing continues after errors:
1. **Panic Mode**: Skip tokens until a synchronizing token (e.g., `;`) is found.
2. **Error Productions**: Define grammar rules for common mistakes (e.g., missing `;`).
3. **Phrase-Level Recovery**: Insert/delete tokens to repair the input.

## Example: Error Recovery in a Simple Parser
```java
// Panic mode example
void parseStatement() {
    try {
        parseAssignment();
    } catch (SyntaxError e) {
        // Skip tokens until ';'
        while (currentToken != SEMICOLON && !eof()) advance();
        consume(SEMICOLON);
    }
}
```
