# Transformer-Encoder-Based-Arabic-Speech-Recognition
This repository holds the implementation for the paper: [Speech recognition based on the transformer's multi‐head attention in Arabic](https://doi.org/10.1007/s10772-024-10092-x).
A pre-print of the published paper is [available](./paper/speech_recognition_based_on_the_transformer_s_multi_head_attention.pdf).
The main contributors in the project are Omayma Mahmoudi and Mohamed Benchat and under the supervision of Mouncef Filali‐Bouami.

## Dataset

The *"Arabic Speech Commands Dataset"*, used within this work, is imported from [this repository](https://github.com/abdulkaderghandoura/arabic-speech-commands-dataset).

### Classes

The following classes are used:

```
classes = ["zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine","right",
 	   "left", "up", "down", "forward", "backward", "yes", "no", "stop", "start", "enable",
 	   "disable", "ok", "cancel", "open", "close", "zoom in", "zoom out", "previous", "next",
 	   "send", "receive", "move", "rotate", "record", "enter", "digit", "direction", "options", "undo"]
```

### Configuration

The training, validation and evaluation of the transformer-based model and the hp tuning is accelerated using a GPU, the following depicts the configuration of the used machine:
```
$ lspci
...
00:00.0 Host bridge: Intel Corporation 8th Gen Core Processor Host Bridge/DRAM Registers (rev 07)
00:01.0 PCI bridge: Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor PCIe Controller (x16) (rev 07)
00:02.0 VGA compatible controller: Intel Corporation UHD Graphics 630 (Mobile)
00:14.2 RAM memory: Intel Corporation Cannon Lake PCH Shared SRAM (rev 10)
00:17.0 SATA controller: Intel Corporation Cannon Lake Mobile PCH SATA AHCI Controller (rev 10)
01:00.0 3D controller: NVIDIA Corporation GP107M [GeForce GTX 1050 Ti Max-Q] (rev a1)
02:00.0 Non-Volatile memory controller: Samsung Electronics Co Ltd NVMe SSD Controller SM981/PM981/PM983

$ cat /proc/cpuinfo
processor	      : x
vendor_id	      : GenuineIntel
cpu family	    : 6
model		        : 158
model name	    : Intel(R) Core(TM) i7-8750H CPU @ 2.20GHz
stepping	      : 10
microcode	      : 0xf0
cpu MHz		      : 800.033
cache size	    : 9216 KB
physical id	    : 0
siblings	      : 12
core id		      : x
cpu cores	      : 6
apicid		      : x
initial apicid	: x
fpu		          : yes
fpu_exception	  : yes
cpuid level	    : 22
wp		          : yes
flags		        : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp lm constant_tsc art arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm 3dnowprefetch cpuid_fault epb invpcid_single pti ssbd ibrs ibpb stibp tpr_shadow vnmi flexpriority ept vpid ept_ad fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid mpx rdseed adx smap clflushopt intel_pt xsaveopt xsavec xgetbv1 xsaves dtherm ida arat pln pts hwp hwp_notify hwp_act_window hwp_epp md_clear flush_l1d arch_capabilities
bugs		        : cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs itlb_multihit srbds mmio_stale_data retbleed
bogomips	      : 4399.99
clflush size	  : 64
cache_alignment	: 64
address sizes	  : 39 bits physical, 48 bits virtual

$ free -h
              total        used        free      shared  buff/cache   available
Mem:           7,6G        5,1G        455M        102M        2,1G        2,1G
Swap:          2,0G        3,5M        2,0G

$ hostnamectl
         Icon name: computer-laptop
           Chassis: laptop
  Operating System: Ubuntu 18.04.6 LTS
            Kernel: Linux 5.4.0-150-generic
      Architecture: x86-64
```

You can follow these steps to start testing the `AudioSpectogram.ipynb` notebook:

1. Create a Python virtual environment, e.g: following these [instructions](https://virtualenv.pypa.io/en/latest/user_guide.html).
  1.1. The used python version:
    ```
    $ python --version
    Python 3.6.9
    ```
2. Install requirements, running the following:
```
pip install -r requirements.txt
```
3. Configure Jupyter Notebook to include your created virtual env following the steps in these [docs](https://ipython.readthedocs.io/en/stable/install/kernel_install.html#kernels-for-different-environments).
4. Run the jupyter notebook, choose the right kernel from the list of kernels in the notebook configuration.
5. Have fun!

### Notes
- The repository also include the parts related to hyperparemater tuning using [Ray Tune](https://docs.ray.io/en/latest/tune/index.html).
- For any feedback, updates or complaints please contact `benchatm@gmail.com` (Mohamed Benchat) or `mahmoudi.omayma@ump.ac.ma` (Omayma Mahmoudi).
- You are very welcome to post issues and help the project grow!
