Cloud Fondry rsh/rcp/rsync to app Utility linux/cygwin
====

## Description
IBM Cloud Cloud Foundry application, rsh rcp rsync

## Usage
* cfssh app-name [options]
* cfscp app-name [options] path1 path2
* cfrsync app-name [options] path1 path

## cfssh Usage
1. remote shell app1  
````
$ cfssh app1
````
2. Socks Server using app1  
````
$ chssh app1 -D :8080
````

## cfscp Usage
1. copy local file1 to remote app1's current directory  
````
$ cfscp app1 file @:.
````
2. copy local dir1 to remote app1's /tmp  
````
$ cfscp app1 -r dir1 @:/tmp/dir1
````
3. copy remote app1's /tmp/dir1 to local  
````
$ cfscp app1 -r @:/tmp/dir1 .
````


## cfrsync Usage 
1. sync local dir1 to app1's remote directory /tmp  
````
$ cfrsync app1 dir1 @:/tmp/
````
2. sync app1's remote directory to local  
````
$ cfrsync app1 @:/tmp/dir1 .
````


## Requirement
* cloud foundry cli tool (cf) `$ cf apps`
* sshpass
cygwin dose not sshpass package. you can get [source](https://sourceforge.net/projects/sshpass/), and compile it.

## Limitation
Only one instance application only.

## Install
copy your path


