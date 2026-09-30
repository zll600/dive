FROM busybox:1.38.0@sha256:fd7dc98638c8e305f4dc34e979f1c0fdfdcaeb0fbf8fcff77ae834b6da3d7e6e
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
