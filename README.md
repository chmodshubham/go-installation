# Golang

You can check out the [official Golang docs](https://go.dev/doc/install) for downloading and installing Go or you can follow the following steps given below.

## Download

- Download the recommended `tar` file to install Go for your system from [here](https://go.dev/doc/install). If you didn't find your operating system, you can download from [this page](https://go.dev/dl/).

## Installation

- If you already have any previous Go Installation in your system, then remove it.

```bash
sudo rm -rf /usr/local/go
```

- Make sure go folder has been removed from `/usr/local/` location. 

```bash
sudo ls /usr/local/
# bin etc games include lib man sbin share src
```

- If you have any go `snap` installed in your system, then remove it.

```bash
sudo snap remove go
```

- Extract the archive you have just downloaded into `/usr/local` so that a fresh new Go tree is created in `/usr/local/go`. 

```bash 
cd Downloads/
sudo tar -xzvf go1.19.linux-amd64.tar.gz --directory=/usr/local/
```

- Add `/usr/local/go/bin` to the PATH environment variable.

```bash
vim ~/.bashrc
```
- Add `export PATH=$PATH:/usr/local/go/bin` command to the end of the script.

![image](https://user-images.githubusercontent.com/97805339/187327748-7b0622e3-703d-44b5-aa41-25912282ba25.png)

- **Note:** Make sure your `GOPATH` and `GOROOT` is not set in this script, if it is, then comment or remove them.

- After saving the changes, `source` the script. `source` is a built-in shell command that reads and executes the file content in the current shell.

```bash
source ~/.bashrc
```

- Check current Go version and make sure it matches with the installed version of Go.

```bash
go version
# go version go1.19 linux/amd64
```
