# Xuepoo's Scoop Bucket

A personal Scoop bucket for Xuepoo's CLI packages. This repository contains Scoop manifests for installing various command-line tools developed by Xuepoo on Windows.

## Installation

First, add this bucket to your Scoop:

```bash
scoop bucket add Xuepoo https://github.com/Xuepoo/scoop-bucket
```

Then install any package from this bucket:

```bash
scoop install Xuepoo/<package-name>
```

## Available Packages

| Package | Description | Version |
|---------|-------------|---------|
| [agent-book-translate](https://github.com/Xuepoo/agent-book-translate) | A powerful LLM-driven agentic EPUB book translator with robust progress monitoring and recovery | 0.1.7 |
| [agent-lx-music](https://github.com/Xuepoo/agent-lx-music) | Intelligent agent-driven music management tools | 0.3.3 |
| [sonic-bridge](https://github.com/Xuepoo/sonic-bridge) | An ultra-fast, lightweight, zero-pretrain-model physical music aesthetic & listening translation middleware for AI Agents & LLMs | 0.6.0 |
| [waywarp_scanner](https://github.com/Xuepoo/waywarp-scanner) | High-performance Wayland GUI layout scanner for AI Agents | 0.1.0 |

## Usage Examples

### Install agent-book-translate
```bash
scoop bucket add Xuepoo https://github.com/Xuepoo/scoop-bucket
scoop install agent-book-translate
```

### Install sonic-bridge
```bash
scoop install sonic-bridge
```

## Updating Packages

To update a package to the latest version:

```bash
scoop update
scoop update <package-name>
```

## Adding New Packages

To add a new package to this bucket:

1. Create a new JSON manifest file in the `bucket/` directory
2. Follow the Scoop manifest conventions
3. Submit a pull request

### Manifest Template

```json
{
  "version": "x.y.z",
  "description": "Short description of the package",
  "homepage": "https://github.com/Xuepoo/package-name",
  "license": "MIT",
  "architecture": {
    "64bit": {
      "url": "https://github.com/Xuepoo/package-name/releases/download/v$version/package-name-windows-x86_64.exe",
      "hash": "HASH_HERE",
      "bin": [["package-name-windows-x86_64.exe", "package-name"]]
    }
  },
  "checkver": {
    "github": "https://github.com/Xuepoo/package-name"
  },
  "autoupdate": {
    "architecture": {
      "64bit": {
        "url": "https://github.com/Xuepoo/package-name/releases/download/v$version/package-name-windows-x86_64.exe"
      }
    }
  }
}
```

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

### Reporting Issues

If you encounter any issues with the packages, please:
1. Check if the issue exists in the original repository
2. If it's a packaging issue, open an issue here
3. Include the package name, version, and error message

### Submitting Pull Requests

1. Fork the repository
2. Create a new branch for your changes
3. Make your changes
4. Test the manifest locally
5. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the Scoop community for the excellent package manager
- Thanks to all contributors who help maintain this bucket

## Contact

- GitHub: [Xuepoo](https://github.com/Xuepoo)
- Repository: [scoop-bucket](https://github.com/Xuepoo/scoop-bucket)