# Albino: a ruby wrapper for pygmentize

This project is an extraction from GitHub.

For this and other extractions, see [http://github.com/github]()

**Note**: This fork has been created specifically to work on Windows, with the intention of 
allowing editing of the local Dartlang site as described on [https://github.com/dart-lang/dartlang.org]()
The only file that has changed is the albino.rb, which you can find in 
C:\ruby\lib\ruby\gems\1.9.1\gems\albino-1.3.3\lib\albino.rb
It uses the work done on these two blogs:
[http://doswa.com/2011/07/19/jekyll-syntax-highlighting-with-pygments-on-arch-linux.html]() and
[http://www.madhur.co.in/blog/2011/09/01/runningjekyllwindows.html]()

**Note**: This library is deprecated in favor of [pygments.rb](https://github.com/tmm1/pygments.rb).

## Installation

    sudo easy_install pygments
    gem install albino

## Usage

### Simple

    require 'albino'
    puts Albino.colorize('puts "Hello World"', :ruby)

### Advanced

    require 'albino'
    @syntaxer = Albino.new(File.new('albino.rb'), :ruby, :bbcode)
    puts @syntaxer.colorize

### Multi

    require 'albino/multi'
    ruby, python = Albino::Multi.colorize([ [:ruby,'1+2'], [:python,'1-2'] ])

