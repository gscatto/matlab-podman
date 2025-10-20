# matlab-podman

Run MATLAB in Podman containers.

## Requirements

- Linux (tested with 6.17.2-arch1-1)
- Podman (tested with version 5.6.2)
- Python (tested with version 3.13.7)

## Installation

Configure the project indicating which MATLAB release name to install  (e.g., `R2025b`) and which toolboxes to make available, separated by spaces (e.g., `Satellite Communications Toolbox, Navigation Toolbox`)

    ./configure R2025b "Satellite Communications Toolbox, Navigation Toolbox"

Prepare the project for installation.

    make

Install the project under `$HOME/.local`.

    make install

## Usage

Search `MATLAB` in the application launcher or `matlab` with auto-completion support in the terminal to discover the available MATLAB versions installed. In the case the application does not come up in the application launcher right away, logout and login.

Containers share `$HOME/Documents/MATLAB` with the host. Also, `$HOME/.MathWorks`, `$HOME/.MATLABConnector`, `$HOME/.matlab` are being mounted for session and settings persistence.

The first run might take a bit to take off. The command `podman ps` may halt until the container starts.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what would you like to change.

## License

[The MIT License](./LICENSE.txt)
