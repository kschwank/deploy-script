deploy-script
=============

Simple shell script that allows copying from and to other machines
using scp as well as showing diffs between local and remote files.

The script loads the mappings from the file deploy.conf in the 
current directory.

The script takes two arguments:

1) a command ("put", "get" or "diff")

2) a mapping id



deploy.conf
-----------

id1:"/path1/file1"->"host2:/path1/file1"

id2:"/path1/file2"->"host3:/path1/file2"

id3:"/path3/file3"->"host3:/path3/file3"


Example:
--------

deploy diff id2

