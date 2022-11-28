# Linux

### Commands with files: 


- list nested files
```bash 
ls -R
```

-  make an archive 
```bash
tar -cf <archive_name>.tar <folder_to_be_archived> 
```

- make an archive with a compression
```bash
tar -czf <archive_name>.tar.gz <folder_to_be_archived> 
```

- list all files in archive 
```bash
tar -tf <archive_name>.tar
```

- unpack/dearchive files
```bash
tar -xf <archive_name>.tar <destination_folder>
```

- decompress/unpack compressed file
```bash
tar -xzf <archive_name>.tar.gz <destination_folder>
```

| **Option** | **Description**                    |
| ------ | ------------------------------ |
| -c     | Create new archive file        |
| -v     | Verbosely list files processed |
| -f     | Archive file name              |


- compress and archive files to a .zip file 
```bash
zip <archive_name>.zip <file_name_to_be_archived>
```

- decompress/unzip files
```bash
unzip <zip_file>.zip
```

- view the content of file
```bash
cat <file_name>.txt
```

- displays the file contents page by page
```bash
more <file_name>.txt
```

```bash
less <file_name>.txt
```


-  to find the number of lines, words and characters in a file
	- The output contains the number of lines followed by number of words followed by number of characters in the file
```bash
wc <file_name>.txt
```
- print only the number of lines
```bash
wc -l <file_name>.txt
```
- To print only the number of words
```bash
wc -w <file_name>.txt
```
- To print only the number of characters
```bash
wc -c <file_name>.txt
```

- view the sorted lines of file 
```bash 
sort <file_name>.txt
```
- To view the reverse-sorted lines
```bash
sort -r <file_name>.txt
```

- View the contents of `file` with equal, consecutive lines merged into one
```bash
uniq <file_name>.txt
```

- The `grep` command allows you to specify a pattern and search for lines from the input text that contain a match to the pattern
```bash
grep `pattern` <file_name>.txt
```

- Some of the frequently used options for `grep` are:
| **Option** | **Description** |
| ------ | ----------- |
|-n |	Along with the matching lines, also print the line numbers
|-c	| Get the count of matching lines
|-i	| Ignore the case of the text while matching
|-v	| Print all lines which do not contain the pattern
|-w	| Match only if the pattern matches whole words 


- The `cut` command allows you to view the lines of a file after a filter is applied to each line. For example, you can use `cut` with the `-c` option to view the first two characters of each line:
```bash
cut -c 2- <file_name>.txt
```
- or each line starting from the second character:
```bash
cut -c 2- <file_name>.txt
```

- The `paste` command allows you to view multiple files at once - with lines being aligned as columns.
```bash 
paste <file_name>.txt <other_file>.txt
```

- You can also customize the delimiter. Instead of the default`tab`, you could specify a comma as follows:
```bash
paste -d "," <file_name>.txt <other_file>.txt
```



### Commands for networking:

- getting your machine' s host name
```bash
hostname
```

- drop the domane suffixe 
```bash
hostname -s
```

- ip address of the hostname 
```bash 
hostname -i
```

- ifconfig (Interface configuration) - Display or configure the system network interface
```bash
ifconfig
```

- info about ethernat adapter 
```bash
ifconfig eth0
```

- send packets known as ICMP (Internet Control Message Protocol) request to the server, listen for a response, and print a result
```bash
ping www.google.com
```

- limited amount of ping results
```bash 
ping -с 5 www.google.com
```

- transfer data to and from URLs
	- returns the entire html code of a page
```bash
curl www.google.com
```

- scrapping a web page's html to a file 
```bash
curl www.google.com -o google.txt
```
```bash
head -n 1 google.txt
```

- download files from URL (and save to a current directory)
```bash 
wget <url_to_file>
```
	- to see first 12 lines of file
```bash
head -n 12 <name_of_file>
```



