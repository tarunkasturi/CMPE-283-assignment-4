# CMPE-283-assignment-4

Nested Paging vs. Shadow Paging

Team Members:
Tarun Pradeep Kasturi (015349685)
Harshit Bhoraskar (015218606)

Contribution of Team members:
1. We worked together over a zoom call to finish the assignment.
2. We ran the assignment-3 again using shadow paging.
3. We ran the code with shadow paging on ept=0.

We used the same assignment-3 environment setup.

1. Start boot the Gues VM.
2. Again reboot the guest VM and record the information from exit count.
3. Turn off Inner VM.
4. Now remove the 'kvm-intel' module from your existing kernal.

              $ rmmod kvm-intel
         
5. Now reload the kvm-intel module with the use of parameter ept=0

              $insmod /lib/modules/5
              /kernal/arch/x86/kvm/kvm-intel.ko ept=0
              
 6. Again boot the Vm, record the exits.
 7. Now again reboot the VM and record the exits.             


## OUTPUT : 
## exit count was printed
CPUID(0X4FFFFFFE), exit number 58 exits=4 </br>
CPUID(0X4FFFFFFE), exit number 59 exits=2 </br>
CPUID(0X4FFFFFFE), exit number 60 exits=0</br>
CPUID(0X4FFFFFFE), exit number 61 exits=0</br>
CPUID(0X4FFFFFFE), exit number 62 exits=0</br>
CPUID(0X4FFFFFFE), exit number 63 exits=3</br>
CPUID(0X4FFFFFFE), exit number 64 exits=3</br>
CPUID(0X4FFFFFFE), exit type 65 is not defined by the SDM</br>
CPUID(0X4FFFFFFE), exit number 66 exits=0</br>
CPUID(0X4FFFFFFE), exit number 67 exits=0</br>
CPUID(0X4FFFFFFE), exit number 68 exits=0</br>

CPUID(0X4FFFFFFE), exit number 12 exits=4</br>
CPUID(0X4FFFFFFE), exit number 10 exits=4</br>
CPUID(0X4FFFFFFE), exit number 3 exits=4</br>
CPUID(0X4FFFFFFE), exit number 1 exits=4</br>
CPUID(0X4FFFFFFE), exit number 2 exits=4</br>
CPUID(0X4FFFFFFE), exit number 4 exits=4</br>
