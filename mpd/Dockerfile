#
# Dockerfile for mpd
#

FROM alpine

#RUN apk add --no-cache mpd mpc && addgroup -S mpdgroup -g 29 && adduser -S mpduser -u 1000 -G mpdgroup && chown mpduser:mpdgroup /var/run/mpd && chown mpduser:mpdgroup /var/lib/mpd && mkdir /playlists && chown mpduser:mpdgroup /playlists
RUN apk add --no-cache mpd mpc
COPY mpd.conf /etc/mpd.conf
VOLUME ["/var/lib/mpd","/music","/playlists"]

EXPOSE 6600
CMD ["mpd", "--stdout", "--no-daemon"]

