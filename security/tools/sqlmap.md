
# sqlmap

## Introduction

sqlmap is an open-source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over of database servers. It is considered as one of the most important tools for pen-testing web applications.

## General Syntax

The basic syntax for using sqlmap is:

```bash
sqlmap [options]
```

where `[options]` could be any of the options described below.

## Options

### Target

- `-u URL, --url=URL`: Target URL (e.g. "http://www.site.com/vuln.php?id=1").
- `-l LOGFILE, --log-file=LOGFILE`: Parse target(s) from Burp or WebScarab proxy log file.
- `-x SITEMAPURL, --sitemap-url=SITEMAPURL`: Parse target(s) from remote sitemap(.xml) file.
- `-m BULKFILE, --bulk-file=BULKFILE`: Scan multiple targets given in a textual file.
- `-r REQUESTFILE, --request=REQUESTFILE`: Load HTTP request from a file.
- `-g GOOGLEDORK, --google-dork=GOOGLEDORK`: Process Google dork results as target URLs.
- `-d DIRECTCONNECTION, --direct=DIRECTCONNECTION`: Connection string for direct database connection.

### Request

- `--data=DATA`: Data string to be sent through POST.
- `--cookie=COOKIE`: HTTP Cookie header value.
- `--random-agent`: Use randomly selected HTTP User-Agent header value.
- `--proxy=PROXY`: Use a proxy to connect to the target URL.
- `--auth-type=ATYPE`: HTTP authentication type (Basic, Digest, NTLM or Certificate).

### Injection

- `-p TESTPARAMETER, --param-del=TESTPARAMETER`: Testable parameter(s).
- `--dbms=DBMS`: Force back-end DBMS to this value.
- `--os=OS`: Force back-end DBMS operating system to this value.
- `--tamper=TAMPER`: Use given script(s) for tampering injection data.

### Detection

- `--level=LEVEL`: Level of tests to perform (1-5, default 1).
- `--risk=RISK`: Risk of tests to perform (0-3, default 1).

### Techniques

- `--technique=TECH`: SQL injection techniques to use (default "BEUSTQ").

### Enumeration

- `-b, --banner`: Retrieve DBMS banner.
- `--current-user`: Retrieve DBMS current user.
- `--current-db`: Retrieve DBMS current database.
- `--passwords`: Enumerate DBMS users password hashes.
- `--tables`: Enumerate DBMS database tables.
- `--columns`: Enumerate DBMS database table columns.
- `--dump`: Dump DBMS database table entries.

## Tamper Scripts

Tamper scripts are used to modify payloads and/or affected request elements before they're sent to the server.

- `apostrophemask.py`: Replaces apostrophe character with its UTF-8 fullwidth counterpart.
- `apostrophenullencode.py`: Appends encoded NULL byte character at the end of the payload.
- `appendnullbyte.py`: Appends URL-encoded NULL byte at the end of the payload.
- `base64encode.py`: Base64 all characters in a given payload.
- `between.py`: Places the SQL keyword BETWEEN the payload and the original value.
- `bluecoat.py`: Used for bypassing Blue Coat proxy AV protection.
- `chardoubleencode.py`: Double URL-encodes all characters in a given payload.
- `charencode.py`: URL-encodes all characters in a given payload.
- `equaltolike.py`: Replaces all occurrences of operator equal with operator LIKE.
- `escapequotes.py`: Slash-escape quotes (`'` and `"`).
- `space2comment.py`: Replaces space character after a SQL keyword with a valid SQL comment.
- `unionalltounion.py`: Replaces UNION ALL SELECT with UNION SELECT.

## Examples

1. For testing whether the 'id' parameter is susceptible to SQL injection:

```bash
sqlmap -u "http://www.example.com/vuln.php?id=1" -p id
```

2. For enumerating databases of a website, where 'id' parameter is susceptible to SQL injection:

```bash
sqlmap -u "http://www.example.com/vuln.php?id=1" --dbs
```

3. For dumping table entries of a website, where 'id' parameter is susceptible to SQL injection:

```bash
sqlmap -u "http://www.example.com/vuln.php?id=1" --dump
```

4. Using sqlmap with POST requests:

```bash
sqlmap -u "http://www.example.com/vuln.php" --data "id=1" -p id
```

5. Using a tamper script to bypass weak string literal escaping:

```bash
sqlmap -u "http://www.example.com/vuln.php?id=1" -p id --tamper=apostrophemask
```

## Further Resources

For further details and options, you can refer to the official documentation of sqlmap at:

```bash
http://sqlmap.org/
```

Please ensure to use this tool responsibly and ethically.
