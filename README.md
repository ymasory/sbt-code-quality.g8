# sbt-code-quality: or, how to use PMD and CheckStyle with sbt #

## Usage ##

- Install [giter8](https://github.com/n8han/giter8).
- Download & run this template.

```sh
$ cd
$ g8 ymasory/sbt-code-quality
$ cd <app name>
$ sbt
> checkstyle
> pmd
```

- Check out `target/checkstyle-report.xml`.
- Check out `target/pmd-report.html`.

## Why not make an sbt plugin? ##

- Why should I?
Most code quality toold have a fully function CLI interface.
An SBT plugin would amount to a ton of boilerplate that replicates the CLI arguments.

- sbt versions are not binary compatible between versions.
They haven't even been source compatible to date.
This way is easier.
