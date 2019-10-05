# SocRSE Trustee Election 2019 Scripts
## Robert Haines and Mark Turner

Scripts to validate and count votes for the SocRSE Trustee Election 2019

## Setup

Clone the repo:

```shell
$ git clone https://github.com/socrse/election-2019-scripts.git
```

To run these scripts you need `ruby` and `rubygems`. On Ubuntu these are both in the `ruby` package:

```shell
# apt-get install ruby
```

Then install `bundler` and get the dependencies:

```shell
$ gem install bundler
$ bundle install
```

## Validating membership

This script takes a list of society members and voters, and produces a list of valid voters and invalid voters based on matching email addresses.

### Usage

Run the script with input from either a file or standard input:

```shell
$ ./validate <csv members file> <csv voters file>
```

## Counting votes

This script takes a validated list of voters and votes, and produces a list of candidates ordered by number of votes. The input list should be in CSV format.

### Usage

Run the script with input from either a file or standard input:

```shell
$ ./count <csv input file>
$ ./count < <csv input>
```
