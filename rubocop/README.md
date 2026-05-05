# Rubocop

The `defaults.yml` config is based on version `0.82.0` of [Rubocop](https://www.rubocop.org) gem ([github](https://github.com/rubocop-hq/rubocop)).

## Usage

To use this config in your project, you need to inherit it by adding:

```yaml
inherit_from:
  - https://raw.githubusercontent.com/Ragnarson/dotfiles/master/rubocop/defaults.yml

inherit_mode:
  merge:
    - Exclude
```

to your `.rubocop.yml`.

After running `rubocop` locally, the inherited (dot)file will be generated. If you don't want to track it with git, add the following to your `.gitignore`:

```gitignore
# Ignore inherited Rubocop config from Ragnarson
.rubocop-9d4d0f74a816c43b8d0a3e80f347d886.yml
```

## Ruby version

To set target Ruby version for Rubocop to use, add this to your projects `.rubocop.yml`:

```yaml
AllCops:
  TargetRubyVersion: 2.7
```

If you don't do this, Ruby version will be taken from `.ruby-version` file.

## Other cops

You may want to consider adding also extensions to Rubocop, like:

- [rubocop-rails](https://github.com/rubocop-hq/rubocop-rails)
- [rubocop-rspec](https://github.com/rubocop-hq/rubocop-rspec)
- [rubocop-performance](https://github.com/rubocop-hq/rubocop-performance)

You can find full list of available extensions [here](https://docs.rubocop.org/en/stable/extensions).

## Contributing

If you want to introduce any changes for `defaults.yml` file, please open a PR.
