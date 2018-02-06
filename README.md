# Tor Docker Example

## Build

Use `image/build` script. Example usage:

    $ image/build ventaquil/tor-docker-example

## Run

Use `image/run` script. Example usage:

    $ image/run ventaquil/tor-docker-example
    
**Attention:** Build image before you try to create container.
    
## Check

If you run container then you can check your `.onion` address using following code:

    $ docker exec [your container name] cat /app/hidden/hostname
    
In response you will get something like `randomstring.onion`. Use curl to check this onion address:

    $ torsocks curl [your onion domain]:8080
    
In response you will get:

    {"success":true}

**Attention:** Remember about 8080 port.
