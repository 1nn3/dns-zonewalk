DNS Zone Walking aka. Yellow Pages

This is a PROOF OF CONCEPT using shell and dig(1) only.

Zone Transfers for Roots and TLDs.

* https://en.wikipedia.org/wiki/DNS_root_zone
* https://en.wikipedia.org/wiki/Root_name_server
* https://en.wikipedia.org/wiki/DNS_zone_transfer

# creates the ./zonefiles directory
time proxychains ./start-zonewalk
or
time proxychains ./zone-transfer <tld> [root server]

du --summarize --total --human-readable ./zonefiles

cat ./zonefiles/*<tld>*.txt* | ./list-domains # | get-html-title -q

See also

* https://github.com/flotwig/TLDR-2
* https://github.com/flotwig/zone-walks


