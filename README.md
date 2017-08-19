## Logy

The best parser for filtering and handling files of any size with ease. Inspecting or filtering large files can be a real pain. Logy let's you open any file in a paginated manner so that there is no overhead of opening the whole file when all you want is searching for a small chunk of text.

## Features

- Written in pure Go (Golang)
- Requires Go > 1.7 to build. Just visit [this link](https://golang.org/doc/install) on how to install Go on your machine
- Deadly simple installation process
- Very easy to use and highly intuitive
- Works on Mac, Linux and Windows

## Installation

```bash
$ git clone git@github.com:iulianclita/logy.git
$ cd logy/
$ go install
```

## Usage

After the file is parsed you can navigate to any page by specifying the desired page number

### Basic usage
```bash
$ logy -file=path/to/file.log # By default it outputs 50 lines per page
```

### Specify how many lines per page
```bash
$ logy -file=path/to/file.log -lines=25 # Now it will output 25 lines per page
```

### Format json output
```bash
$ logy -file=path/to/file.log -text=json # Every json structure that is found will be nicely formatted 
```

### Search for text
```bash
$ logy -file=path/to/file.log -filter=Exception # Every text that is found will be nicely colored to be easily observed 
``` 

### Navigate to any page
```bash
$ logy -file=path/to/file.log -page=10 # The parser will directly navigate to the specified page number 
```

### Enable regex support
```bash
$ logy -file=path/to/file.log -filter=[0-9]{2}:[0-9]{2}:[0-9]{2} --with-regex # The parser will search for any text that matches whatever was specified in the filter option flag
```  

### Disable colored output of any kind
```bash
$ logy -file=path/to/file.log --no-color # The parser will display all text with the same color (black/white). Probably you will never want this behavior but it's here just in case :)
``` 

Of course all the flag options can becombined in any manner to obtain the desired results
