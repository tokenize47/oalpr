# oalpr
OpenALPR license plate reader for RaspberryPi

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
