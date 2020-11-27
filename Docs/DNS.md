# DNS Tools Tips/Tricks

## Easy to read SPF TXT DNS Records.

### Linux CLI Only:

The below BASH function takes a domain's TXT records and makes the SPF Record more human readable.

    $ dig +short txt somedomain.com
    "google-site-verification=TCtQARZdwqYz00QUGEaqKG6TpDRPxLnA0xjvOr1L7WE"
    "v=spf1 include:eu._netblocks.mimecast.com include:mktomail.com include:sendgrid.net include:sent-via.netsuite.com include:_spf.salesforce.com include:docebosaas.com -all"
    "_globalsign-domain-verification=GeBngTn9j8-utE2irGheYZSAXx6u5iGMQcd_tKlAgN"
    "docusign=a975f19c-4ea8-4d81-a277-b1c8eac0b50c"

    $ dug() { dig +short txt $1 | grep -P "^\"v=spf1" | perl -pe 's/\" \"//g;s/\s+/\ /g;s/ /\n/g' | perl -pe 's/\"v=spf1//g;s/.all\"//g;s/\"//g' | perl -pe 's/^\ $//g'; };

    $ dug somedomain.com
    spf.protection.outlook.com
    include:eu._netblocks.mimecast.com
    include:mktomail.com
    include:sendgrid.net
    include:sent-via.netsuite.com
    include:_spf.salesforce.com
    include:docebosaas.com

**NOTE**: There is a query limit of 10 total for SPF reocords.

- [rfc4408](https://datatracker.ietf.org/doc/rfc4408/?include_text=1)

  - Found in "10.1. Processing Limits"

    SPF implementations MUST limit the number of mechanisms and modifiers
    that do DNS lookups to at most 10 per SPF check, including any
    lookups caused by the use of the "include" mechanism or the
    "redirect" modifier. If this number is exceeded during a check, a
    PermError MUST be returned. The "include", "a", "mx", "ptr", and
    "exists" mechanisms as well as the "redirect" modifier do count
    against this limit. The "all", "ip4", and "ip6" mechanisms do not
    require DNS lookups and therefore do not count against this limit.
    The "exp" modifier does not count against this limit because the DNS
    lookup to fetch the explanation string occurs after the SPF record
    has been evaluated.

    When evaluating the "mx" and "ptr" mechanisms, or the %{p} macro,
    there MUST be a limit of no more than 10 MX or PTR RRs looked up and
    checked.

    SPF implementations SHOULD limit the total amount of data obtained
    from the DNS queries. For example, when DNS over TCP or EDNS0 are
    available, there may need to be an explicit limit to how much data
    will be accepted to prevent excessive bandwidth usage or memory usage
    and DoS attacks.

## Why can't I get all of the records for a domain?

