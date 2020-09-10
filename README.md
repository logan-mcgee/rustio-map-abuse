# rustio-map-abuse

some info about how the API of playrust.io can be used to gain an advantage against others.

## NOTE: THESE ARE SIMPLY CONCEPTS. NO CODE WILL BE SHARED ON HOW TO DO SUCH THINGS

### Using their system for creating 'death heatmaps' as a way of tracking current pvp

`/deaths.json` contains data about deaths so that the website can update heatmaps with this info. however, this require the client to be aware of death locations, this means we can pull the x and z, alongisde the death reason, in order to 'track' deaths.

For example, if we see a user die to an explosion at 512, 250, we can convert these values into grid references, and know where a raid could be occuring. 

Not only can we do that, encouraging a user to kill a teammate would also allow for us to know the base location of that user.

### Finding monuments easily (used to use for triple cave base locations)

`/monuments.json` shows extra data about monuments than the actual website. for example, hovering over a cave on the page shows that its simple a 'cave' wheras using their API you can tell exactly the cave. This isnt a big issue in any capacity, but still super useful for having the perfect cave/etc for your base.

### Connecting to the websocket for extra data

`/ms` is the websocket endpoint which deals with the data for live deaths, connections, etc. This is pretty useless in terms of exploitability, but could be used for trying to figure out the person who died in `/deaths.json` for example, as this one shows the steamid and username of the death, whereas deaths does not.
