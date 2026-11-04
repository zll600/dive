FROM busybox:1.38.0@sha256:a46257e06c82ad85242d0d38077d0a52d9896389ca60a1a59d3463db586e5fa4
ADD example.md /somefile.txt
RUN mkdir -p /root/example/really/nested
RUN cp /somefile.txt /root/example/somefile1.txt
RUN chmod 444 /root/example/somefile1.txt
RUN cp /somefile.txt /root/example/somefile2.txt
RUN cp /somefile.txt /root/example/somefile3.txt
RUN mv /root/example/somefile3.txt /root/saved.txt
RUN cp /root/saved.txt /root/.saved.txt
RUN chmod +x /root/saved.txt
RUN chmod 421 /root
RUN rm -rf /root/example/
ADD overwrite.md /root/saved.txt
