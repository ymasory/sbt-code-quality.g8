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

## Customize ##

- Change the CLI args (`val args`) in `CheckStyleSettings` and `PmdSettings` in
`project/build.scala` in the generated projects.
See the [CheckStyle CLI](http://checkstyle.sourceforge.net/cmdline.html)
documentation and the [PMD CLI](http://pmd.sourceforge.net/running.html)
documentation.
- Tweak or replace `project/checkstyle-config.xml` and `project/pmd-ruleset.xml` in the generated project with something appropriate for your requirements. See the [CheckStyle](http://checkstyle.sourceforge.net/config.html) and [PMD](http://pmd.sourceforge.net/howtomakearuleset.html) XML configuration docs.

## Why not make an sbt plugin? ##

- Why should I?
Most code quality toold have a fully function CLI interface.
An sbt plugin would amount to a ton of boilerplate that replicates the CLI
functionality.
- sbt versions are not binary compatible between versions.
They haven't even been source compatible to date.
This way is easier.
- This same strategy can be used to quickly spit out new CLI-based tasks.
