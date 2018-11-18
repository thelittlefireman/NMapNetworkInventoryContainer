# NMap Network Inventory Container
Have you ever wanted up-to-date NMap scan data in an easily understandable format? Have you noticed how hard it is to get that? So did I! So I hacked together a docker container to continually scan (about every 2 Hours) your network and display the findings cleanly using Debian, [Namp Grepable Output](https://nmap.org/book/output-formats-grepable-output.html), A bash script to convert it to a CSV and some [D3.js code](https://d3js.org/).

## Build and Run Instructions

#### Clone
`git clone https://github.com/thelittlefireman/NMapNetworkInventoryContainer`

#### Run
`docker run --name nmap-inventory -t -p 1337:1337 inventory`

You can add `-e OPTIONS "-sV"` and `-e TARGETS "192.168.1.0/24"` and change by what you want

#### Enjoy
After the first run is complete (it will take a while) you can access the website [here](http://127.0.0.1:1337).

It will look like this:
![Screenshot](https://raw.githubusercontent.com/jgamblin/NMapNetworkInventoryContainer/master/ScreenShot.png)

#### Important Notice
I likely don't know what I am doing and this could be done faster, better and simpler some other way. Also make sure you have permission to NMap something before you do!
