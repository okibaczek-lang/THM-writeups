# THM ROOM - Content discovery

## Common files

- robots.txt - owners of the site often leaves there valuable data which arent secured and can be viewed by unauthorized users

- sitemap.xml - tells search engines which pages the owner wants listed, unsecured can be viewed by other users which can lead to data leakege

## Search engines

- google dorking - lets you browse information about a site (by using filters) that aren't visible with normal browsing

- Wappalyzer - defines the technologies on the website

- Wayback machine - archive, can show old target sites

- S3 bucket - cloud storage, misconfigurated can lead to data leakege. URL format https://{name}.s3.amazonaws.com
 - common naming patterns : {company}-assets, {company}-backup, {company}-www, and {company}-dev

## Automated discovery

- gobuster is an open-source enumeration tool written in Go. Usage:
 - gobuster dns -d site -w FILE --wildcard(for dns)
 - gobuster dir -u site -w FILE(for directories)
 - gobuster vhost -u site --domain domain -w FILE --append-domain --exclude-length 250-320(for vhosts)
  - u = Target URL
  - d = Target domain
  -w = Wordlist
  - --wildcard = Ignore wildcard DNS responses
  - --domain = Specify the target domain
  - --append-domain = Append the domain to each wordlist entry
  - --exclude-lengt` = Exclude responses with specific content lengths

 ## Key lesson

 You don't have to start with immedatelay ,,hacking" into target
 You can start with research using open source intelligence avaible on the internet
