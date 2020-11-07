# Easy to read SPF TXT DNS Records.

## Linux Only:

    $ dug() { dig +short txt $1 | grep -P "^\"v=spf1" | perl -pe 's/\" \"//g;s/\s+/\ /g;s/ /\n/g' | perl -pe 's/\"v=spf1//g;s/.all\"//g;s/\"//g' | perl -pe 's/^\ $//g'; };

    $ dug somedomain.com
    spf.protection.outlook.com
    include:eu._netblocks.mimecast.com
    include:mktomail.com
    include:sendgrid.net
    include:sent-via.netsuite.com
    include:_spf.salesforce.com
    include:docebosaas.com
