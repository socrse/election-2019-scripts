# SocRSE Trustee Elections Reporting
## Robert Haines and Mark Turner

Validate and count votes for the SocRSE Trustee Elections.

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

## Creating the election report

This script takes a list of society members and voters, and produces a report containing the result of the election. The default report shows full detail, including the numbers of votes cast for each candidate. A redacted report can also be generated, which just shows who is elected and who is not. The script validates the votes against the list of members, and then counts the number of votes for each candidate.

The full report also includes details of any invalid votes received; the redacted report simply shows numbers of invalid votes.

### Usage

Run the script, providing the correct inputs. To create a full report, simply:

```shell
$ ./report <csv members file> <csv voters file>
```

Add the `-r` or `--redact` flag to create a redacted report. You can get full details of all report options by using the `-h`, `-?` or `--help` flags.

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
