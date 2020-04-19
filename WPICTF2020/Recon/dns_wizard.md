# dns_wizard
> Can you find it?

> made by: acurless


Since we're talking about DNS, and without any nameserver, my first reflex was to use dig on the ctf website

	dig any wpictf.xyz
	
One line of the output got my attention:
> wpictf.xyz.		3788	IN	HINFO	"RFC8482" ""

RFC document or "Request For Coment" are documents publied by the IETF that describe Networking protocols or materials. The name of RFC8482 is interesting:
> "Providing Minimal-Sized Responses to DNS Queries That Have QTYPE=ANY"

Because they refer to this particular RFC, we can infer that using dig with an "any" argument won't work. I supposed the flag would probably be in a TXT format and tried:
	
	dig txt wpictf.xyz

This gave me the folowing input:

> wpictf.xyz.		299	IN	TXT	"V1BJezFGMHVuZF9UaDNfRE5TLXJlY29yZH0="

This String format look like base64 so I put it in a base64 decoder and got the string "WPI{1F0und\_Th3\_DNS-record}"

**flag** :WPI{1F0und\_Th3\_DNS-record}
  
  