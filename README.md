# pachube-stream

Creates a streaming TCP connection with pachube TCP API SERVER

## Installation

Use NPM:

    npm install pachube-stream # I have not push to NPM yet so you cannot do this yet

Otherwise just use npm to link yourself
    
    git clone http://github.com/carboncalculated/node-pachube-stream.git
    cd node-pachube-stream
    npm install pachube-stream -l # local 

## Methods And Events

See the [TCP Streaming API docs][api-docs] for exactly that

[api-docs]: http://api.pachube.com/v2/beta/#tcp-socket-and-websocket-connections

## Usage (coffee)
  
  {Connection} = require("pachube-stream")

  @con = new Connection("Your API KEY")

  @con.on "error", (error) ->
    console.log(error)

  subscription = @con.subscribe("/feeds/7049")

  subscription.on "complete", (data) ->
    console.log(data)

  subscription.on "data", (data) ->
    console.log(data)

## TODO

* Reconnections
* Other Methods GET ETC
* Finish off Tests
* Push to NPM

## Note on Patches/Pull Requests (Standard)
 
* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with version or history.
  (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches.

## Copyright

Copyright (c) 2011 Richard Hooker. See LICENSE for details.
