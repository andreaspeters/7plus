[]--------------------------------------------------[]
|     7PLUS - file converter for store & forward     |
| * no commercial use * no sale * circulate freely * |
| version 2.25/LFN (20000320) (C) Axel Bauda, DG1BBQ |
[]--------------------------------------------------[]

Commands (more exact descriptions, see manual): 

7plus file   <-- 'file' must not carry an extension (.7pl/.p01/.cor etc.)
  Automagic mode. 7PLUS will look for the right files and try to decode
  and correct, if possible. If a non-7PLUS file named 'file' exists, 7PLUS
  will encode it.

7plus file.txt
  Encode 'file.txt' (automatically split into 10K chunks).

  Valid options for encoding:

  -s 30      30 lines/part (max 512 lines/part).
  -sp 3      3 parts of roughly equal size (max 255 parts).
  -sb 3000   Parts of roughly 3000 bytes (max 36000).
  -r 5-10,1  When encoding, only create part 5 through 10 and part 1.
             Be sure to split the same way as for the first upload!
  -t /ex     Append string '/ex' to encoded files (BBS file termination).
  -send "sp dg1bbq @db0ver" Add send command for BBS (-send2 = 2 line send).
  -tb file   Get head and footlines from format file 'file' when encoding.
             Produces ready-for-upload files. See manual.
  -j         Join all parts into a single output file 'file.upl'.

7plus file.err /pr/
  Create correction file. Look for original unencoded file in '/pr/'.
  Omit path of original unencoded file, if it's in the current directory.

7plus file.err file2.err -j
  Add contents of error report 'file2.err' to error report 'file.err'.
  If second filename is omitted, 7PLUS will look for 'file.e01', 'file.e02'
  etc and add their contents to 'file.err' (automatic multiple join).
  Joining of err-files is necessary for producing collective cor-files.

7plus file.7ix
  Create new error report from indexfile, if it's been accidentally erased.

7plus logfile -x text
  Extract 7PLUS files from 'logfile'. Only extract a file, if its name
  contains 'text'. Omit 'text' to extract all files in 'logfile'.

7plus file.err /pr/
  Create correction file. Look for original unencoded file in '/pr/'.
  Omit path of original unencoded file, if it's in the current directory.

7plus file.err file2.err -j
  Add contents of error report 'file2.err' to error report 'file.err'.
  If second filename is omitted, 7PLUS will look for 'file.e01', 'file.e02'
  etc and add their contents to 'file.err' (automatic multiple join).
  Joining of err-files is necessary for producing collective cor-files.

7plus file.7ix
  Create new error report from indexfile, if it's been accidentally erased.

7plus logfile -x text
  Extract 7PLUS files from 'logfile'. Only extract a file, if its name
  contains 'text'. Omit 'text' to extract all files in 'logfile'.

Other Options (not all options listed):

-k    Automatically kill all obsolete files.
-p    Use Packet line separator CR for encoded files. Should be used,
      when uploading files to the BBS in binary mode! See manual.
-y    Assume YES on all queries.

And do me a great favor: READ THE MANUAL, PLEASE! 73s, Axel.


This GIT repo is handled by HB9XAR to keep this software alive.
