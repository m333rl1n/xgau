# Xgau
A tool for crawl web pages, get URLs from waybackurls and parse BurpSuite output.
```
$ ./xgau
usage: xgau.py [-h] [-b BURP] [-w] [-p] [-k KATANA] target

Crawl webpage, use waybackmachine and crawl BurpSuite result to find URLs and
parameters.

positional arguments:
  target                URL or domain.

optional arguments:
  -h, --help            show this help message and exit
  -b BURP, --burp BURP  BurpSuite XML output.
  -w, --wayback         Get URLs from waybackmachine.
  -p, --passive         Get URLs from waybackmachine.
  -k KATANA, --katana KATANA
                        Extra katana switches.
```
### Requirements:
- go
- python3 

### Usage

1. clone repo:
```bash
git clone https://github.com/m333rl1n/xgau.git
cd xgau
```
2. copy katana config:
```
mkdir -p ~/.config/katana/
cat ./field-config.yaml >> ~/.config/katana/field-config.yaml
```
3. crawl a web page:
```
$ ./xgau 'https://example.com' -w 
# result:
[+] Search in WaybackMachine
[+] Active crawling ...
[+] URLs are at example.com-urls.txt
[+] Paramters are at example.com-params.txt
```
