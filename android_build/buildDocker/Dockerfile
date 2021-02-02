FROM tiwater/android_build_env:14.04
ARG userid
ARG groupid
ARG username
RUN groupadd -g $groupid $username \
 && useradd -m -u $userid -g $groupid $username \
 && echo $username >/root/username
ENV HOME=/home/$username
ENV USER=$username
USER $username
ENTRYPOINT ["/bin/bash"]
CMD ["-i"]
