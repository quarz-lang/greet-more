# greet-more

A second example cog for [Quarz](https://quarz.dev), depending on
[greet](https://github.com/quarz-lang/greet) 1.1.0. An application that
asks for greet 1.0.0 and also uses greet-more gets greet 1.1.0: Quarz
chooses, for each cog, the highest of the lowest versions asked for
(minimal version selection).

```toml
# Cog.toml of an application
[dependencies]
Greet     = { git = "https://github.com/quarz-lang/greet", tag = "v1.0.0" }
GreetMore = { git = "https://github.com/quarz-lang/greet-more", tag = "v1.1.0" }
```

```ruby
puts GreetMore.farewell("Quarz")   # => Goodbye, Quarz. (greet-more 1.1.0)
```

`quarz test` runs its tests. Licensed under MIT No Attribution (LICENSE).
