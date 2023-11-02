

Subdomain Enumeration (Alt alan adı numaralandırma) nedir?  

Alt alan adı numaralandırma, bir veya daha fazla alan adı için alt alan adları bulma işlemidir. Keşif aşamasının önemli bir parçasıdır.

 - Brute Force Enumeration
 
1)  gobuster dns -t 30 -w <wordlist dosya yolu> -d x.x.x.x

-dns: DNS subdomain bruteforcing mode.
-d: target domain.
-t <n>: number of concurrent threads (default 10).
-w <wordlist>`: path to the wordlist.

2)  amass enum -brute -w subdomains.txt -d example.com -o results.txt

-brute: Execute brute forcing after searches.
-w: Path to wordlist file.
-d: Domain names separated by commas.
-o`: Path to the text file containing terminal stdout/stderr

