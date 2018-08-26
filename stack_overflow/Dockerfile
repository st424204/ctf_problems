FROM ubuntu:16.04
RUN apt update 
RUN apt install xinetd -y
RUN useradd -m pwn
COPY share/* /home/pwn/
COPY pwn /etc/xinetd.d/pwn
RUN chmod 774 /tmp
RUN chmod -R 774 /var/tmp
RUN chmod -R 774 /dev
RUN chmod -R 774 /run
RUN chown -R root:root /home/pwn

CMD ["/usr/sbin/xinetd","-dontfork"]
