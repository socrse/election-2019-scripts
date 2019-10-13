# frozen_string_literal: true

# (c) 2019 The Society of Research Software Engineering
#
# Authors: Robert Haines and Mark Turner

SCRIPT = ::File.expand_path('report', __dir__)
REPORTS = ['report', 'report-redacted'].freeze

desc 'build the markdown reports'
task :md do
  REPORTS.each do |file|
    sh "#{SCRIPT} members.csv votes.csv"
  end
end

desc 'build the PDF reports'
task :pdf do
  REPORTS.each do |file|
    sh "pandoc #{file}.md -o #{file}.pdf"
  end
end

desc 'build all reports'
task report: [:md, :pdf]

task default: :report
