This repository houses a the **concourse**, or *universe of possible* statements/items about the economy, taxation and related/additional topics.

[Wikipedia](http://en.wikipedia.org/wiki/Q_methodology) describes a *concourse* as:

> "the sum of all things people say or think about the issue being investigated"

A sample from this concourse may be used for [q-sorts](http://qmethod.org) on the economy, taxation and related/additional topics, such as [`keyneson-sample`](https://github.com/maxheld83/keyneson-sample).

This concourse was originally developed and first used as part of [Maximilian Held's](http://www.maxheld.de) [dissertation](http://www.maxheld.de/schumpeter) on taxation and democracy, and was be administered before and after [Civicon](http://www.civicon.de) Citizen Conferences on the topic.

The genesis and logic of this concourse is documented in the [wiki](https://github.com/maxheld83/keyneson-concourse/wiki), which is also included here as a submodule.


## Contributing

Everyone is welcome to comment on and improve this project.
Please file pull requests and issues.

Please note:


### Files

- The item formulations in this concourse sit in `language.csv`, with one file for every language.
	This is the *only* place where actual items formulations are entered or edited.


### Columns

These files always includes only *three* columns:

1. `Item-ID`, some string that *uniquely* identifies the item across all related studies or language for q-sort administration and data entry.
	`Item-IDs` are also printed on the actual q-cards for administering the q-sort.
	In contrast to `Item-Abbreviation`, they should not contain any cues about their content but only random gibberish so as not to influence the participants.
2. `Item-Abbreviation` is meant for q-sampling (of statements) and for analyses and thus should be both *unique* across all q-sorts and q-studies and *meaningful to humans*, so that researchers can readily make sense of items when sampling or analysing.
   Something like `people-incentives` might be a good `Item-Abbreviation`.
3. `Item-Full`, the complete item formulation in the language identified by the file name, as it would appear to study participants.


### Edits vs Additions

If you *edit* an item, just, ... well ... edit it.
Please do not change `Item-Abbreviation` or `Item-ID` into `C102-v1.2` or something like that – git and releases take care of this kind of versioning automatically.

If you want to *add* a new item, just add a new line with a unique `Item-ID` and `Item-Abbreviation`.

In the borderline case of substantive changes to an *existing* item, ask yourself whether you would like:

- the new version to *replace* the old one for everybody (edit a line)
- or just offer the item as an *alternative* (add a new line)


### Q-Sampling & Metadata

For any particular q-sort or study, you will of course need to draw, and justify, a sample from these statements.

This is *not* done in this repository, but in some other repository, such as [`keyneson-sample`](https://github.com/maxheld83/keyneson-sample), which in turn, includes this concourse as a submodule.
In these other repositories with the sample, you can refer to items from this concourse by their `Item-Abbreviation` *only*; there's no need to copy items.

The same applies to any kind of metadata (tags) that you might want to add.

This is done so as to:

a) keep concourse and q-sample analytically distinct, as they were intended by Stephenson to be
b) to allow parallel development of different samples based on the *same* universal concourse with partial (and interesting!) overlap.
c) to keep this repo neat and applicable to a wide range of research projects.


### Different Languages

This q concourse can/should be extended into several languages, all of which can be maintained in this single repository as per the following rules:

1. The baseline item formulations, as well as all metadata should always be in english (!), so that everyone understands a minimum of what a new item is about.
2. Only the filed `Item-Full` in `*.csv` is translated.
	*Everything else*, including `Item-Abbreviation`, is always in english, and always the same across different languages.
3. Everything added to `master` should be available at least in *english* and (optionally) one parallel translation.
	Branches and Pull requests will be merged into `master` only if they have achieve language parallelity (?).


### Releases

This repo includes releases only for convenient referencing and a precise DOI; they really don't make a lot of sense as there are no binaries to be shared here, and any commit to master should be fine by itself anyway.