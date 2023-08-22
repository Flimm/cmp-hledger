# cmp-hledger

[nvim-cmp](https://github.com/hrsh7th/nvim-cmp) source for [hledger](https://hledger.org/) accounts.

cmp-hledger completes based on prefix and prefix abbreviation (e.g. `E:D:C` to `Expenses:Drinks:Coffee`) of hledger account names.

## Setup

You will need [Neovim](https://neovim.io/) and [hledger](https://hledger.org/) to be installed using whatever method you prefer. To install these packages using yay, run:

```shell
yay -S neovim hledger
```

You will also need [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) to be installed and configured.

Now, install `cmp-hledger` with your favorite package manager for Neovim. For example, if you're using the [`packer.nvim`](https://github.com/wbthomason/packer.nvim) package manager, add this line to the configuration of Neovim:

```lua
use('kirasok/cmp-hledger')
```

Then, configure `nvim-cmp` to include `cmp-hledger` as a source, using configuration like this:

```lua
-- Set configuration for .ledger files
cmp.setup.filetype('ledger', {
  sources = cmp.config.sources({
    {
      name = 'hledger',
    }
  })
})
```


## [ledger](https://github.com/ledger/ledger) support

Plugin will choose to work with `ledger` if it won't find `hledger` binary in `PATH`.

## License

Source code available under [GNU GENERAL PUBLIC LICENSE](https://www.gnu.org/licenses).

## Credits

Thanks [cmp-beancount](https://github.com/crispgm/cmp-beancount) for providng example of making [cmp](https://github.com/hrsh7th/nvim-cmp) source.
