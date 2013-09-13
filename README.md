deploy-script
=============

Simple shell script that allows copying from and to other machines
using scp as well as showing diffs between local and remote files.

The script loads the mappings from the file .deployrc in the 
current directory.

The script takes two arguments:

1) a command ("put", "get", "diff" and "edit")

2) a mapping id

"put" will copy the local file to its mapped location

"get" will copy the remote file to its local location

"diff" will download the remote file to a temporary file 
  and show the diff between that file and the local file

"edit" will start 'vim' with the local file.

deploy.conf
-----------

id1:"/path1/file1"->"host2:/path1/file1"

id2:"/path1/file2"->"host3:/path1/file2"

id3:"/path3/file3"->"host3:/path3/file3"


Example:
--------

deploy diff id2

