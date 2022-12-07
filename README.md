# [WIP] Starship Primer

## Introduction

A configuration preset for [Starship](https://github.com/starship/starship).

- Colors are copied from [Primer Light Theme](https://primer.style/primitives/colors).
- Programming language/tools background colors are the official color of each one.
- The left column contains only: `username`, `directory`, `git_branch`, `git_status`. The remaining ones are in the right column.

## Supported languages/tools/configurations

- Username.
- Git.
- Time.
- Languages and tools:
  - C.
  - Kubernetes.
  - Google Cloud.
  - Go.
  - Java.
  - Lua.
  - NodeJS.
  - PHP.
  - Python.
  - Rust.
- Command duration.
- Character.

Reference documentation: https://starship.rs/config/.

## Supported Terminals

Below is the list of tested environments.

| OS    | Terminal                                                          | Supported?     | Tested Environment               |
| ----- | ----------------------------------------------------------------- | -------------- | -------------------------------- |
| macOS | [Alacritty](https://github.com/alacritty/alacritty)               | ✅             | Alacritty v0.11.0                |
| macOS | [iTerm2](https://github.com/gnachman/iTerm2)                      | ✅             | iTerm2 v3.4.18                   |
| macOS | [Tabby](https://github.com/Eugeny/tabby)                          | ✅             | Tabby v1.0.187 (Alpha 187)       |
| macOS | [VSCode Integrated Terminal](https://github.com/microsoft/vscode) | ✅ (partially) | VSCode v1.73.1                   |
| macOS | [WezTerm](https://github.com/wez/wezterm)                         | ✅             | WezTerm 20221119-145034-49b9839f |

## Screenshots

Alacritty

![Alacritty](screenshots/alacritty_0001.png)

iTerm2

![iTerm2](screenshots/iterm2_0001.png)

Tabby

![Tabby](screenshots/tabby_0001.png)

VSCode

![VSCode](screenshots/vscode_0001.png)

WezTerm

![WezTerm](screenshots/wezterm_0001.png)

## How to use it?

- At this moment, you must copy configurations from [starship.toml](./starship.toml) to your existing Starship configuration.
- You can copy file [starship.toml](./starship.toml) to the default Starship configuration location (~/.config/starship.toml).
- An easier way for a basic user, add this line into your shell init script (`~/.zshrc`, `~/.bashrc`). In the future, you just need to pull updated commits from our repository and your Starship configurations will be updated automatically.
  ```
  export STARSHIP_CONFIG=/path/to/this/repository/starship.toml
  ```
- Remember to change to a font that supports Powerline icons.
- Currently, the screenshots are using the font `MesloLGS NF`. You can download it from [here](https://github.com/romkatv/powerlevel10k#fonts).

## How to contribute?

- This project needs your help to add more configurations for missing programming languages and tools.

- Recommended steps:

  - Fork this project

    ```
    git clone git@github.com:ansidev/starship-primer.git
    ```

  - Modify configurations in [starship.toml](./starship.toml).
    - Color hex code should use `lowercase`.
    - Text color should be `#ffffff` or `#000000` depending on the background color.
  - Add test files corresponding to the configurations.
  - Open the terminal and change the working directory to this project's root directory.
  - Run the below command to temporarily switch to the local Starship config for testing purposes (closing the terminal will restore your own Starship config).
    ```
    source test.sh
    ```
  - The terminal working directory will be changed to `test` automatically after running the above command. You need to check whether everything works well.
  - If everything is OK:
    - Add the supported languages/tools/configurations, and tested environment to [README.md](./README.md).
    - Update screenshot(s) to `screenshots` for each tested environment.
  - Commit and push changes to your repository.
  - Create a PR (you should create 1 PR per programming language/tool/configuration).

## Contact

Le Minh Tri [@ansidev](https://ansidev.xyz/about).

## License

This source code is available under the [AGPL-3.0 LICENSE](/LICENSE).
