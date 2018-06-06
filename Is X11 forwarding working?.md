# Root
A log of code and notes for using root in the Mignerey lab
Is X11 forwarding working?
type b=new TBrowser() into root once it has loaded


If get error:
***Display not set, setting it to 194.12.147.164:0.0
then it spits out after several minutes In case you run from a remote ssh session, recconnect with SSH -Y

FIX: 
In putty go to SSH then X11
then in X display location type    
localhost0
