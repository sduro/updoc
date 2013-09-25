updoc
=====

Subir un fichero a google docs
Source: http://planzero.org/blog/2012/04/13/uploading_any_file_to_google_docs_with_python

Here's a sample of the output, where the file backup_2012-04-13.tar.bz2 was uploaded to the Backups collection:

=$ ./gupload.py backup_2012-04-13.tar.bz2 Backups

Google Docs Upload Tool - v0.1 - http://planzero.org/
o Logging in... success!
o Fetching collection ID... success!
o Uploading file... success!
Uploaded 11.72 MiB in 17.75 seconds
$ 
To use the script, all you need to do is fill in your username and password and make sure recent 
versions of the gdata library and the magic module are installed (see the comments at the top of the 
script for specifics). When you run the tool the collection name parameter is optional, if you don't 
provide it the file will be uploaded to your root collection. Note that the collection name is case sensitive, 
so if you get an error about the collection not being found, double check the case first!

It should be fairly easy from this base to incorporate OAuth authentication and other goodies.
For my part, I'm going to expand the script to automatically create and upload a nice tarball containing 
a backup of important files on the server each night as part of a cron job. That should make my client's 
life a little easier :-)

Enjoy!
