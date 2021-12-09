# CMPE-283-assignment-4

Nested Paging vs. Shadow Paging

Team Members:
Tarun Pradeep Kasturi (015349685)
Harshit Bhoraskar (

Contribution of Team members:
1.We run the code back in assignment-3 with using shadow paging.
2. We run the code with shadow paging on ept=0.

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
