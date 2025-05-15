# NOS - Noesis Open Shell

`nos` is a fork of the [fish shell](https://fishshell.com/) that provides all the features you love about fish while allowing for innovation and experimentation beyond the original codebase.

## Key Features

- **Full fish compatibility** - All your existing fish scripts, completions, and configurations continue to work in nos
- **Extension independence** - Introduce new features and syntax without breaking compatibility
- **Upstream synchronization** - Easily integrate upstream fish shell improvements

## Dual Extension System

The core innovation in nos is the dual extension system that allows for a seamless compatibility layer:

### How It Works

- Files can have either `.fish` or `.nos` extensions
- When nos looks for a function, completion, or configuration file:
  1. It first looks for a `.nos` file
  2. If no `.nos` file exists, it falls back to the `.fish` file

This approach lets you:
- Keep using all existing fish shell resources
- Gradually migrate to nos-specific features at your own pace
- Create nos-specific implementations without modifying fish functionality

```
functions/
├── git.fish    # Original fish function
└── git.nos     # Enhanced nos version (takes precedence)
```

## Why Fork?

This fork allows us to:

1. **Evolve independently** - Introduce new features without being constrained by fish's compatibility requirements
2. **Mitigate dependency risks** - If fish development were to slow down or stop, nos can continue evolving
3. **Maintain compatibility** - Your investment in fish scripts and knowledge isn't lost
4. **Experiment freely** - Test new ideas without the constraints of the fish codebase

## Getting Started

### Installation

```fish
git clone https://github.com/yourusername/nos.git
cd nos
make
sudo make install
```

### Using .nos Files

1. Create a `.nos` file in the same location as the `.fish` file you want to override
2. The nos shell will automatically use your `.nos` file instead of the `.fish` file

### Migration Example

To migrate a fish function to nos:

```fish
# Original: ~/.config/fish/functions/prompt_git.fish
function prompt_git
    echo "Fish git prompt"
end

# Enhanced: ~/.config/fish/functions/prompt_git.nos  
function prompt_git
    echo "Enhanced nos git prompt with more features"
end
```

## Contributing

Contributions to nos are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

nos is licensed under the same terms as fish shell. See [COPYING](COPYING) for details.

## Acknowledgments

- The fish shell team for creating the amazing foundation that nos builds upon
- All contributors to nos and the fish shell
