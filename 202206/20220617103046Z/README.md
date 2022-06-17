# EBPF

ref: https://ebpf.io/

What:
Runs through a privileged process, makes use of hooks and allows to easily
monitor and control OS wide processes, greatly helping with applications focused
on security, observability and network

Why:
Useful to get around the need for kernel changes and updates, which are commonly slow,
and understandbly so, due to security and stability reasons, Kernel modules are
also an option but have a very busy maintenance cycle due to the need to update
whenever a new kernel version is released

Using:
BCC, Cillium, libbpf, are some toolchains commonly use to interact with ebpf, as
they provide easier abstraction than the default EBPF APIs

> tags: ebpf; bcc; libbpf;

> uid: 20220617103046Z

> links: 

