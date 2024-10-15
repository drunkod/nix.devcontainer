To enable Nix Flakes in your NixOS configuration, you need to follow these steps:

### 1. Enable Experimental Features

#### For Non-NixOS Systems:

If you are using Nix on a non-NixOS system, you can enable flakes by modifying your Nix configuration file, usually located at `~/.config/nix/nix.conf`:

0. create folder ~/.config/nix:
   ```bash
   mkdir ~/.config/nix
   ```
1. Open or create the `nix.conf` file:
   ```bash
   nano ~/.config/nix/nix.conf
   ```

2. Add the following line:
   ```conf
   experimental-features = flakes nix-command
   ```

3. Save the file and exit the editor.

### 2. Verify Flakes are Enabled

To verify that flakes are enabled, you can run the following command:
```bash
nix flake --help
```
If flakes are enabled, you should see the help output for the flake command.

### 3. Using Flakes

Once flakes are enabled, you can start using them. For example, you can create a new flake with:
```bash
nix flake init
```
Or you can use existing flakes from GitHub or other sources.




# nix.university
1. <a href="https://codespaces.new/preston-johnson/nix.university" target="_blank">Click here to start a Codespace on nix.university/main</a>
2. Open a Terminal ( Ctrl + Backtick ) and pick a path below.

### nix repl
- Type `nix repl`
- Hit [Enter]
- (Optionally, type `university = import ./university.nix` then hit [Enter] again)

### nix-shell
- Type `nix-shell`
- Hit [Enter] (This loads shell.nix, which provides Emacs)

> [!IMPORTANT]
> If the above steps do not work as expected, then please reach out!

Note: including Nix language extensions in .devcontainer.json crashes the build, so they need to be installed afterward.
