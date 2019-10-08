# SocRSE Trustee Election 2019 Report
## Robert Haines and Mark Turner

Validate and count votes for the SocRSE Trustee Election 2019.

## Setup

Clone the repo:

```shell
$ git clone https://github.com/socrse/election-2019-scripts.git
```

To run this report you need `ruby` and `rubygems`. On Ubuntu these are both in the `ruby` package:

```shell
# apt-get install ruby
```

Then install `bundler` and get the dependencies:

```shell
$ gem install bundler
$ bundle install
```

## Creating the election report

This script takes a list of society members and voters, and produces a report containing the result of the election. It validates the votes against the list of members, and then counts the number of votes for each candidate.

The report includes details of any invalid votes received.

### Usage

Run the script, providing the correct inputs:

```shell
$ ./report <csv members file> <csv voters file>
```
