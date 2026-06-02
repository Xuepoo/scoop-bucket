# Contributing to Xuepoo's Scoop Bucket

Thank you for your interest in contributing to this Scoop bucket! This document provides guidelines and information for contributors.

## How to Contribute

### Reporting Issues

If you encounter any issues with the packages, please:

1. Check if the issue exists in the original repository
2. If it's a packaging issue, open an issue in this repository
3. Use the issue template provided
4. Include the package name, version, and error message

### Submitting Pull Requests

1. Fork the repository
2. Create a new branch for your changes
3. Make your changes
4. Test the manifest locally
5. Submit a pull request using the provided template

## Development Guidelines

### Manifest Conventions

- Follow Scoop's manifest conventions
- Use consistent formatting
- Include proper descriptions
- Add autoupdate when possible
- Update version numbers correctly

### Testing Manifests

Before submitting a manifest, test it locally:

```bash
# Install from local manifest
scoop install ./bucket/package-name.json

# Test autoupdate
scoop update package-name

# Check for style issues
 scoop lint ./bucket/package-name.json
```

### Adding New Packages

To add a new package:

1. Create a new JSON manifest file in the `bucket/` directory
2. Use the manifest template from the README
3. Include proper metadata (description, homepage, license)
4. Add installation instructions for Windows
5. Include autoupdate configuration

### Updating Existing Packages

To update an existing package:

1. Update the version number
2. Update the download URLs
3. Update the hash values
4. Test the updated manifest

## Code Style

### JSON Style

- Use 2 spaces for indentation
- Follow JSON style guidelines
- Use consistent naming conventions
- Add comments for complex logic (JSON doesn't support comments, so use clear structure)

### Manifest Structure

```json
{
  "version": "x.y.z",
  "description": "Description",
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

## Release Process

### Version Updates

1. Update the manifest with new version
2. Update download URLs
3. Update hash values
4. Test the manifest
5. Submit a pull request

### Testing Releases

Before releasing:

1. Test on Windows 10/11
2. Verify all downloads work
3. Run the autoupdate check
4. Test the binary execution

## Community Guidelines

### Be Respectful

- Be respectful to other contributors
- Provide constructive feedback
- Help others when possible

### Communication

- Use clear and concise language
- Provide detailed information in issues
- Respond to comments in a timely manner

## Getting Help

If you need help:

1. Check the Scoop documentation
2. Look at existing manifests for examples
3. Open an issue for questions
4. Join the Scoop community

## License

By contributing to this project, you agree that your contributions will be licensed under the MIT License.

## Acknowledgments

- Thanks to the Scoop community
- Thanks to all contributors
- Thanks to users who report issues