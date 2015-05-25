A set of CSV files containing the constituencies, candidates, and results from
the general election held in the United Kingdom on 7 May 2015, collected as a
[data package] [1].

---

The data, sourced from the [BBC] [2] and [The Economist] [3], comprises two CSV
files, `constituencies.csv` and `candidates.csv`. Both files can be found in the
`data` sub-directory.

The `constituencies.csv` file contains details on the 650 UK constituencies that
each elected one MP at the general election. Each row matches a single
constituency. The file contains seven columns:

* `constituency_id`: unique code for a constituency, provided by the Office for
  National Statistics
* `name`: formal name of the constituency
* `region`: in England, the sub-national geographical region in which the
   constituency lies; in Scotland, Wales, and Northern Ireland, the country name
* `electorate`: number of people registered to vote in the constituency
* `turnout`: number of valid votes counted in the constituency
* `status`: whether or not the candidate who won the seat came from a party
  different to his or her predecessor
* `swing`: extent of change in voter support since the 2010 election

The `candidates.csv` file contains details on each candidate that stood for
election in one of the 650 UK constituencies. Each row in the file matches a
single, unique, candidate. The file contains five columns:

* `constituency_id`: unique code for the constituency in which the candidate
  stood for election; this matches the column of the same name in
  `constituencies.csv`
* `party`: name of the political party for which the candidate stood
* `candidate`: candidate’s own name
* `votes`: number of valid votes cast for the candidate
* `vote_share`: valid votes cast for the candidate divided by valid votes cast
  in the constituency, expressed as a percentage

The two files can be joined using the `constituency_id` column found in each.
The primary key for `constituencies.csv` is the `constituency_id` column, while
for `candidates.csv` it’s a combination of the `constituency_id`, `party`, and
`candidate` columns.


# Licence

The raw numbers are in the public domain, but the data package itself is
released under the [Creative Commons Attribution-ShareAlike 4.0 licence] [4],
which is included in the accompanying `LICENSE` file.


# Home page

The latest version of this data can be found at
https://github.com/flother/uk-general-election-2015.


# Changelog

    2015-05-25: Version 1.0 released


[1]: http://dataprotocols.org/data-packages/
[2]: http://www.bbc.com/news/election/2015/results
[3]: http://www.economist.com/uk2015data
[4]: https://creativecommons.org/licenses/by-sa/4.0/
