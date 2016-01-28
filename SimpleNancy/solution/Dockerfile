FROM            mono:4.2.1
COPY            . /src
WORKDIR         /src
RUN             xbuild SimpleNancy.sln
EXPOSE          8081
CMD             ["mono",  "SimpleNancy.SelfHost/bin/Debug/SimpleNancy.SelfHost.exe" ]