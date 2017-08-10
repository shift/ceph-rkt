# Ceph Rkt

The following unit files are used to deploy Ceph onto CoreOS

## Prerequisites

TLS enabled etcd running on the same host, with TLS keys (`etcd-ca.crt`, `etcd-client.crt`, `etcd-client.key`) in `/etc/ssl`.
Unused/zero'd disks for Object Storage Daemons

The following defined in `/etc/environment`:
 * `MON_IP`, should be the IP of the internal interface or private IP including port (eg. `192.168.45.10:6789`).
 * `CEPH_PUBLIC_NETWORK`, should be the netmask of the network upon which the clients connect (eg. `192.168.45.0/24`).
 * `CEPH_PRIVATE_NETWORK`, should be the netmask of the network upon which the storage network operates (eg. `192.168.45.0/24`).


