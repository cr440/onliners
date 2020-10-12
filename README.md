# onliners

### Convert curl command to ffuf 
- add wordlist
- add **FUZZing** place
- add **-u** before url
- add other flags
```sh
c2f(){
    cat $1 | sed 's/curl -i -s -k/ffuf -w/' | sed 's/\$//g' | sed 's/--data-binary/-d/' >> $1.ffuf; pluma $1.ffuf
}
```