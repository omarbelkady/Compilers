### Security 

## Theory
Compilers enforce security through:
1. **Stack Canaries**: Detect buffer overflows with runtime checks.
2. **ASLR**: Randomize memory addresses to thwart exploits.
3. **Sanitizers**: Instrument code to catch memory corruption (e.g., AddressSanitizer).

## Example: Stack Canary in GCC
```c
// Compile with -fstack-protector
void foo(char *src) {
    char buf[128];
    strcpy(buf, src); // Stack canary checks for overflow
}
```