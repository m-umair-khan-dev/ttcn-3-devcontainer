# TTCN-3 Devcontainer

A Development Docker Container for TTCN-3 development using the Eclipse Titan toolset.

## Overview

This Dev Container provides a pre-configured environment for working with TTCN-3 using the Eclipse Titan compiler and tools. It simplifies the setup process, ensuring that all dependencies are installed and configured correctly.

## Features

- Based on Alpine Linux for a lightweight environment
- Pre-installed dependencies for TTCN-3 development
- Pre-configured user (`titan`) with sudo privileges
- Automatic host modification at startup
- Pre-configured VS Code settings and extensions
- Integrated with Git for version control

## Getting Started

### Prerequisites

- [VS Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- [Docker](https://www.docker.com/) installed on your system

### Usage
To launch locally, ensure the prerequisites are met


1. Clone this repository:
   ```sh
   git clone https://github.com/m-umair-khan-dev/ttcn-3-devcontainer.git
   cd ttcn-3-devcontainer
   ```

2. Open the folder in VS Code.

3. When prompted, click **"Reopen in Container"** or manually open the Command Palette (`Ctrl+Shift+P`) and select **"Dev Containers: Reopen in Container"**.

4. Start working with TTCN-3!

## Repository Structure

```
├── .devcontainer/         # Dev Container configuration
│   ├── devcontainer.json  # Dev Container settings
└── NOTES.md               # Documentation
```

## Development Environment

### Installed Tools

- `Eclipse Titan TTCN-3` (cloned and built from source)
- `gcc`, `make`, `git`
- `diffutils`, `expect`, `openssl-dev`, `libxml2-dev`
- `ncurses-dev`, `flex`, `bison`, `perl`, `bash`, `libedit`
- `lksctp-tools` (for SCTP protocol testing)

### VS Code Customizations

The `devcontainer.json` file ensures a seamless development experience with:

- Default shell set to `bash`
- Installed extensions:
  - C/C++ (ms-vscode.cpptools)
  - GitLens (ms-vscode.gitlens)
  - Makefile Tools (ms-vscode.makefile-tools)

### Post-Creation Setup

After the container starts, the `.bashrc` script updates the `/etc/hosts` file for proper hostname resolution.

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to enhance this Dev Container.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## References

- [Eclipse Titan](https://www.eclipse.org/titan/)
- [TTCN-3 Testing](https://en.wikipedia.org/wiki/Testing_and_Test_Control_Notation)
- [VS Code Dev Containers](https://code.visualstudio.com/docs/remote/containers)
