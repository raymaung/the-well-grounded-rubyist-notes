# The Well Ground Rubyist

## Chapter 1 - Bootstrapping your Ruby Literacy

### 1.1.2 The variety of Ruby identifiers

* Variables:
    * Local
    * Instance variable
        * Storing information for individual objects 
        * Always start with `@`, ie. `@age` `@last_name`
        * Use *snake_case* by convention
    * Class variable 
      * Storing information *per* class hierarchy
      * Start with `@@`, ie. `@@running_total`
      * Use *snake_case* by convention
    * Global variable
      * Recognizable by their leading dollar sign `$`
      * Use all upper case by convention
      * `$POPULATION`


### 1.1.5

* `-cw` to check syntax
    * `ruby -cw my_ruby.rb`

### 1.2 Anatomy of the Ruby Installation

* To get *ruby* installation files location in irb session
    * `irb --simple-prompt -rrbconfig` 
    * Ruby command line tools `>> RbConfig::CONFIG["bindir"]`
    * Ruby standard library `>> RbConfig::CONFIG["rubylibdir"]`

    
    
### 1.3.2 Load Paths

* `$:` (dollar - colon) provides a list of directories to searh for `load`
* `load` does not automatically search for the current director
    * require explicit path with `./` to indicate current directory
* `load` loads files for *each* time it is called

### 1.4.3 ri and RDoc

#### RI

* `ri String#upcase` to see documentation on `String.upcase`
* `#` indicates looking for instance method
* Run in Unix `pager` mode, use `-T` to output without filtering through pager
    * `ri -T String#upcase` 

### RDoc
* Ruby Documentation System
* `rdoc` to scan comments and generate nicely formatted documentation


### 1.4.4 The rake task-management utility#### Rake
* `make`-inspired task- management utility
* `rake --tasks` to list all defined tasks

#### 1.4.5 Installing packages with the gem command
* `gem install prawn`
    * Look for the gem in the current direcotry
    * Local cache maintained by the RubyGems system
        * Use `-l` option to restrict to the local file system
    * Get from the remote
        * `-r` (remote) to only install from remote
* `gem uninstall prawn`
    * To uninstall gem     
* Can also install a gem from a gem file residing locally on your hard disk
    * `gem install /home/me/mygems/ruport-1.4.0.gem`
    * 

##### LOADING AND USING GEMS

* `requrie "prawn"` to add gem to the initial load path (`$:`)
    * ```
        require "prawn"

        puts $:.grep(/hoe/) 
    ```

