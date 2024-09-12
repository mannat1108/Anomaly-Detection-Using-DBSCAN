# Anomaly-Detection-Using-DBSCAN

This repository contains the implementation of anomaly detection using the DBSCAN (Density-Based Spatial Clustering of Applications with Noise) algorithm. DBSCAN is an unsupervised clustering algorithm particularly effective for detecting outliers and anomalies in datasets by grouping together points that are closely packed together, marking points that lie alone in low-density regions as outliers.

Table of Contents-
1)Introduction
2)Dataset

Introduction-
The purpose of this project is to identify anomalies in a given dataset using the DBSCAN algorithm. Unlike traditional clustering methods, DBSCAN can automatically determine the number of clusters based on the density of data points and can effectively handle noise (anomalies).

Key Features:
Unsupervised anomaly detection
Automatic determination of the number of clusters
Detection of noise/outliers
Handles clusters of varying shapes and sizes


- Explanation of Dataset attributes/features:¶
Duration: duration of connection(in seconds)

protocol_type: type of protocol (tcp, icmp, udp)

Service: Network type (private, ftp_data, eco_i, telnet, http, smtp, ftp, ldap, pop_3, courier, discard, ecr_i, imap4, domain_u, mtp, systat, iso_tsap, other, csnet_ns, finger, uucp, whois, netbios_ns, link, Z39_50, sunrpc, auth, netbios_dgm, uucp_path, vmnet, domain, name, pop_2, http_443, urp_i, login, gopher, exec, time, remote_job, ssh, kshell, sql_net, shell, hostnames, echo, daytime, pm_dump, IRC, netstat, ctf, nntp, netbios_ssn, tim_i, supdup, bgp, nnsp, rje, printer, efs, X11, ntp_u, klogin, tftp_u)

Flag: Flag status (REJ, SF, RSTO, S0, RSTR, SH, S3, S2, S1, RSTOS0, OTH)

Src_bytes: Number of bytes transferred from source to destination

Dst_bytes: Number of bytes transferred from destination to source

Land: If connection is to same host land=1, else 0

Wrong_fragment: Number of wrong fragments (0, 1, 3)

Urgent: Number of urgent packets (0, 1, 2, 3)

Hot: Number of “hot” indicators (0, 1, 2, 3, 4, 5, 6, 7, 10, 11, 15, 18, 19, 22, 30, 101)

Num_failed_logins: Number of failed logins (0, 1, 2, 3, 4)
Logged_in: If logged in logged_in=1, else 0
num_compromised: Number of compromised conditions (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 14, 15, 23, 25, 36, 49, 57, 165, 381, 611, 796)
root_shell: If root shell is obtained root_shell=1, else 0
su_attempted: If “su root” accesses, su_attempted=1, else 0
num_root: Number of accessed roots (0, 1, 2, 3, 4, 5, 7, 8, 9, 17, 23, 26, 31, 45, 51, 145, 173, 401, 684, 878)
num_file_creations: Number of file creations (0, 1, 2, 3, 4, 5, 6, 7, 100)
num_shells: Number of shell prompt (0, 1, 2, 5)
num_access_files: Number of operations on access files (0, 1, 2, 3, 4)
num_outbound_cmds: Number of outbound commands
is_host_login: If login is hot is_host_login=1, else 0
is_guest_login: If login is guest is_guest_login=1, else 0
Count No.: Number of connections to the same host in last 2 seconds
srv_count: Number of connections to the same service in last 2 seconds
serror_rate: Percentage of connection with syn error
srv_serror_rate: Percentage of connection with syn error
rerror_rate: Percentage of connection with rej error
srv_rerror_rate: Percentage of connection with rej error
same_srv_rate: Percentage of connection of same service
diff_srv_rate: Percentage of connection of different service
srv_diff_host_rate: Percentage of connection of different hosts
dst_host_count: Number of connections of same destination host
dst_host_srv_count: Number of connections of same destination host and service
dst_host_same_srv_rate: Percentage of connections having same destination host and service
dst_host_diff_srv_rate: Percentage of connections having different service on current host
dst_host_same_src_port_rate: Percentage of connections of current host having same src port
dst_host_srv_diff_host_rate: Percentage of connection of same service and different hosts
dst_host_serror_rate: Percentage of connections of current host having S0 error
dst_host_srv_serror_rate: Percentage of connections of current host of a service having S0 error
dst_host_rerror_rate: Percentage of connections of current host that have rst error
dst_host_srv_rerror_rate: Percentage of connections of current host of service that have rst error
Attack: Type of attack (apache2, back, buffer_overflow, ftp_write, guess_passwd, httptunnel, imap, ipsweep, land, loadmodule, mailbomb, mscan, multihop, named, neptune, nmap, normal, perl, phf, pod, portsweep, processtable, ps, rootkit, saint, satan, sendmail, smurf, snmpgetattack, snmpguess, sqlattack, teardrop, udpstorm, warezmaster, worm, xlock, xsnoop, xterm)
Level: Threat level of the attack (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21)
