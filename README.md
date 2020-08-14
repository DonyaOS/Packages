# Packages

## Donya Package System

The distribution employs a package system based around the concept of easily
parseable plain-text files (with fields separated by lines and spaces).

This format allows effortless interface using any programming language or just
basic UNIX utilities and tools.

## Package Structure

```
zlib/            # Package name.                  
- build          # Build script (chmod +x).       
- sources        # Remote and local sources.      
- version        # Package version.               

Optional files:

- depends        # Dependencies (usually required).
- pre-remove     # Pre-remove script (chmod +x).
- post-install   # Post-install script (chmod +x).
- patches/*      # Directory to store patches.
- files/*        # Directory to store misc files.
```

### Contribution

Please make sure to read the Contributing Guide before making a pull request. If you have a Donya-related project/feature/tool, add it with a pull request to this curated list!

Thank you to all the people who already contributed to DonyaOS!

### License

**MIT**
