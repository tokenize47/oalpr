# oalpr
OpenALPR license plate reader for RaspberryPi

The whole idea around this image is to provide a working environment with OpenALPR for a RaspberryPi. The interaction between the tool and the host can be performed by python so take a look into the oalpr.py file to see an example of how to do it. The run command below mounts some volumes based on the example code.

Usage:
<br/>
You can provide folders to override the scripts and check the log.
<br/>
<code>
docker run --name=oalpr \
    -p 5000:5000 \
    -v /etc/localtime:/etc/localtime:ro \
    -v /root/cctv/data:/root/oalpr/data \
    -v /root/cctv/log:/root/oalpr/log \
    -v /root/cctv/scripts:/root/oalpr/scripts \
    -v /root/cctv/conf:/etc/openalpr \
    --restart=always \
    --detach=true \
    tokenize/oalpr
</code>
