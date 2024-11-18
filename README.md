# f5ssl-decrypt

### Description

This script combines the steps stated in [K31793632](https://my.f5.com/manage/s/article/K31793632) and [K42350941](https://my.f5.com/manage/s/article/K42350941). End result is you can open output_tcpdump_file with wireshark without specify the pms file to decrypt TLS data.


### Before using

1. Copy script to Quantum $HOME/bin and Set your PATH (https://www.architectryan.com/2012/10/02/add-to-the-path-on-mac-os-x-mountain-lion/#.Uydjga1dXDg)

2. Make file executable (https://gcore.com/learning/how-to-make-file-executable-in-linux)\
>sudo chmod 755 $HOME/bin/f5ssl-decrypt

### Usage

**Make sure current working directory has Read/Write access for the files to be created**

In Quantum, change your working directory and copy pcap files to /sr/<case_number>/working.

```
blow@hostname:/case/12345678/working$ f5ssl-decrypt *.pcap
====================================================================================================
IMPORTANT: Current working directory must have RW permission otherwise file can't be created
====================================================================================================

capture1.pcap: CREATED -> capture1.pcap.pms and capture1_tlsinject.pcap

capture2.pcap: CREATED -> capture2.pcap.pms and capture2_tlsinject.pcap
```
