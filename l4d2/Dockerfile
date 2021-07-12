FROM cm2network/steamcmd

RUN ~/steamcmd/steamcmd.sh +login anonymous +force_install_dir ../l4d2 +app_update 222860 +quit

USER steam
EXPOSE 27015/udp

COPY server.cfg /home/steam/l4d2/left4dead2/cfg

ENTRYPOINT ["/home/steam/l4d2/srcds_run", "-console", "-usercon", "-game", "left4dead2", "-port", "27015", "-secure", "+maxplayers", "4"]
