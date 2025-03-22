# Alex's supply-chain source

Supply-chain source for [cargo-vet][] to ensure third-party dependencies have been audited by trusted entity.


* Aggregated list of audits by trusted sources such as [Mozilla][] and [Embark Studios][Embark],
* Audits of third-party crates by me,
* Skeptically crafted audits of first-party crates.


This repository automatically [aggregates][aggregates-doc] audits from trusted sources to make them easily reusable by me and others.

To import this source into another [cargo-vet][] instance, add the following lines to your `config.toml`:

```toml
[imports.boozook]
url = "https://raw.githubusercontent.com/boozook/supply-chain/main/audits.toml"
```

or run command

```sh
cargo vet import boozook https://raw.githubusercontent.com/boozook/supply-chain/main/audits.toml # --verbose=info
```


[cargo-vet]: https://mozilla.github.io/cargo-vet
[Mozilla]: https://github.com/mozilla/supply-chain
[Embark]: https://github.com/EmbarkStudios/rust-ecosystem
[aggregates-doc]: https://mozilla.github.io/cargo-vet/multiple-repositories.html
