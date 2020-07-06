FROM java-env


RUN curl -SL -# http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/oxygen/2/eclipse-jee-oxygen-2-linux-gtk-x86_64.tar.gz | tar -xz

RUN export uid=1000 gid=1000 && \
mkdir -p /home/developer/workspace && \
echo "developer:x:${uid}:${gid}:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
echo "developer ALL=(All) NOPASSWD: ALL" >> /etc/sudoers && \
chmod 0440 /etc/sudoers && \
chown ${uid}:${gid} -R /home/developer/workspace

USER developer
ENV HOME /home/developer 
