# TRACEROUTE
This project is my traceroute command personnalisation.

## RESUME
Traceroute (or tracert on Windows) is a utility program that lets you
follow the paths that a data packet (IP packet) will take to get from there
local machine to another machine connected to the IP network. It was designed within the
Lawrence-Berkeley National Laboratory.

## BEHAVIOUR

ft_traceroute [ -4 ] [ -f first_ttl ] [ -m max_ttl ] [ -N squeries ] [ -p port ] [ -w waittime ] [ -q nqueries ] [ -z sendwait ] host [ packetlen ]
```c
	-4				Use IPv4
	-I				Use ICMP ECHO for tracerouting.
	-f first_ttl	Start from the first_ttl hop (instead from 1).
	-m max_ttl		Set the max number of hops (max TTL to be rached). Default is 30.
	-N squeries		Set the number of probes to be tried simultaneously (default is 16).
	-p port			Set the destination port to use. It is either initial udp port value for "default" method (incremented by each probe, default is 33434, or initial seq for "icmp" (incremented as well, default from 1), or some constant destination port for other methods (with default of 80 for "tcp", 53 for "udp", etc.).
	-w waittime		Set the number of seconds to wait for response to a probe (default is 5.0). Non-integer (float point) values allowed too.
	-q nqueries		Set the number of probes per each hop. Default is 3
	-z sendwait		Minimal time interval between probes (default 0). If the value is more than 10, then it specifies a number in milliseconds, else it is a number of seconds (float point values allowed too).
	-U 				Use UDP to particular port for tracerouting (instead of increasing the port per each probe), default port is 53.
	-h				Read this help and exit.

Arguments:

	host			The host to traceroute to
	packetlen		The full packet length (default is the length of an IP header plus 40). Can be ignored or increased to a minimal allowed value.
```

## AUTHOR(s)
+ gilles Bourgeois