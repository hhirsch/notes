# Podman
I was checking out different container management systems and I really liked the deamonless nature of podman.
I also like the added isolation that comes with rootless containers.

At first I found it a bit hard to find official documentation about Quadlets but I found it in the man page
`man "podman-systemd.unit"`.

For development or temporary mapping from my rootless podman containers to a privileged port like 80 I am
using socat like this:
`socat TCP-LISTEN:80,reuseaddr,fork TCP:127.0.0.1:8080`

When I am done I kill it with *Ctrl+c*.
