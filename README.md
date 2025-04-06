# AX - Action Executor

Define and execute commands in a workspace scope.

## Installation

```shell
# This command assumes "$HOME/.local/bin" is in PATH. Any other path can be used.
curl --fail -o "$HOME/.local/bin/ax" "https://raw.githubusercontent.com/deohayer/ax/main/ax"
chmod +x "$HOME/.local/bin/ax"
```

## Usage

```shell
# Initialize a workspace in a current directory.
# Create .ax subdirectory with a template script.
ax --init
# Setup completion (modifies .bashrc).
ax --setup
# Reset completion (modifies .bashrc).
ax --reset
# Update to the latest version.
ax --update
# Print info.
ax -@
# Print hint.
ax -!
# Print help.
ax -?
```

Inside a workspace, `ax` can be used to run any non-hidden `.sh` script in `.ax`.
Assuming that `.ax` contains a script `cmd.sh`:

```shell
# Run the command, can be run from any subdirectory of the workspace.
ax cmd
# Print help (if available).
ax cmd -?
```
