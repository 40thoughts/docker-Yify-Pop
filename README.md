# Yify-Pop

The purpose of the Yify-Pop image is to provide you a `Popcorn-Time`-like app usable with your browser from your local desktop or a remote server.

## Table of contents

- [Run](#run)
- [Have fun](#have-fun)

## Run

* Just run the image by executing this command :

        sudo docker run -d --name yify-pop -p 4000:4000 -p 8889:8889 -p 8890:8890 -p 8891:8891 -p 8892:8892 crazybud/yify-pop

It runs a container called `yify-pop` as demon with port `4000` as http and the others for stream sources (4 in this exemple).
It's up to you to add ports for allowing more clients to watch at the same time.
Just use this port range : `8889-8999` and add them in incremental order since `yify-pop` looks for open ports in this range, I noticed that in this setup, each stream launched just takes the next port in the range.

Please, avoid to change default ports (4000 and 8889) you may have some bugs for the moment.

## Have fun

And now, open your navigator and type this in the adress bar : `http://<host ip>:4000`.<br/>
If you installed this container on your desktop just type `http://localhost:4000` or [click here](http://localhost:4000)

That's it !!!
