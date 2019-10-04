# SoC RSE Election 2019 Scripts
## Robert Haines and Mark Turner

Scripts to validate and count votes for the Soc RSE Trustee Elections 2019

### Get the code

Clone the repo:

```shell
$ git clone https://github.com/socrse/election-2019-scripts.git
```

## Validating membership

Under construction.

## Counting votes

This script takes a validated list of voters and votes, and produces a list of candidates ordered by number of votes. The input list should be in CSV format.

### Usage

To run this script you need `ruby` and `rubygems`. On Ubuntu these are both in the `ruby` package:

```shell
# apt-get install ruby
```

Then install `bundler`:

```shell
$ gem install bundler
```

Then move into the `counting` directory and install the script's dependencies:

```shell
$ cd counting
$ bundle install
```

To run the script:

```shell
$ ./count <csv input file>
```
