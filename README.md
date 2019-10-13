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
$ sudo apt-get install ruby
```

Then install `bundler` and get the dependencies:

```shell
$ gem install bundler
$ bundle install
```

## Creating the election reports

This script takes a list of society members and voters, and produces two reports containing the result of the election; one is a full report, the second (redacted) does not display the numbers of votes cast for each candidate. The script validates the votes against the list of members, and then counts the number of votes for each candidate.

The reports include details of any invalid votes received.

### Usage

Run the script, providing the correct inputs:

```shell
$ ./report <csv members file> <csv voters file>
```

The reports can be turned into PDF format using `pandoc`:

```shell
$ pandoc report.md -o report.pdf
$ pandoc report-redacted.md -o report-redacted.pdf
```

You can also use `rake` to build the PDF reports:

```shell
$ rake pdf
```

If you name the members file `members.csv`, and the voters file `votes.csv`, then you can run the whole process within `rake`:

```shell
$ rake
```

See the `Rakefile` for more details.
