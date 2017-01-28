# idid

idid, as in I did, records a searchable changelog over time.
multiuser, multipurpose, git based and easy to pipe to grep.

## help

    git based simple changelog for use with grep. multiple users can use 
    this tool as long they remember to pull and push to a central repository.
    set environment variable IDID_STORE to change the changelog store folder 
    location.

    set IDID_SUBFOLDER environment variable or use the -d option to change 
    the default store subfolder.

    this program is heavly inspired from pass, the standard unix password 
    manager. look at https://www.passwordstore.org/. 

    version:
        0.9
        
    author:
        arnulf heimsbakk
        https://github.com/aheimsbakk/idid
        
    usage:
        $PRG add [-a] [-y] [-d subfolder] changelog free text 
            add a changelog line in the the specified directory structure.
            
            -a  mark log entry as done from script, automatic 
            -d  destination directory for changelog, if not specified
                it defaults to bash \$USER variable, currently "$USER"
            -y  answer yes to all questons

        $PRG list [subfolder]
            list directory structure and changelog files.
            
        $PRG log [-a|subfolder] [partial date]
            list changelog, filter on subfolder and parts of a date on the
            format 1970-01-01. 
            
            -a  list all change log lines without filtering
            
        $PRG tags [-a|subfolder] [partial date]
            list #- and @-tags in the changelog, filter on subfolder and 
            parts of a date on the format 1970-01-01.
            
        $PRG help
            show this help screen

        $PRG example
            show some examples of usage
            
        $PRG version
            show current version 
            
        $PRG
            list last week of logs

