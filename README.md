## rubocop-ruleset

This gem simply exists to contain a .rubocop.yml which I can share among projects.

The contents themselves simply disable rules deemed excessive, ugly, made-up etc.

### Usage

* Depend on this gem as a git dependency in your Gemfile
* Have a .rubocop.yml file with contents such as:

```yml
inherit_gem:
  rubocop-ruleset: .rubocop.yml

AllCops:
  TargetRubyVersion: 2.5
  Exclude:
    - "db/schema.rb"
  UseCache: false

Layout/TrailingWhitespace:
  Enabled: false
Layout/TrailingBlankLines:
  Enabled: false
```

As illustrated by the last two rules, using this gem doesn't impede overriding or adding more rules.
