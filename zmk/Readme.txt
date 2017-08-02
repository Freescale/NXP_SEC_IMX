1. Introduction about the demo:
	This application is a linux user space code, which is a zmk programming example

2. Build instructions:
   
   It is compiled with tool chain as below:
   $ source /home/b32331/mcu/toolchains/fsl-imx-xwayland-glibc-x86_64-fsl-image-gui-cortexa9hf-neon-toolchain-4.1.15-2.0.0/environment-setup-cortexa9hf-neon-poky-linux-gnueabi
   $ make clean
   $ make
   
3. Run instructions:

root@imx6qdlsolo:~/zmk# ./zmk

         ZMK Programming Example

[INFO]   SNVS_HPVIDR1=0x3e0100, SNVS_HPVIDR2=0x0
[INFO]            SNVS_HPVIDR1[IP_ID,MAJOR_REV,MINOR_REV]=[0x3e, 0x1, 0x0]
[INFO]   A.1. Checking transition SSM (System Security Monitor - see SNVS_HPSR[SSM_ST]) from check state to functional state (trusted/secure/non-secure)
[INFO]           System Security Monitor is in Non-Secure mode
[INFo]   A.2. Set the correct value in the Power Glitch Detector Register.
[INFO]           SNVS_LPPGDR power glitch before init 0x41736166
[INFO]           SNVS_LPPGDR power glitch after init 0x41736166
[INFO]   A.3. Clear the power glitch record in the LP Status Register.
[INFO]           SNVS_LPSR  before init 0x40000000
[INFO]           SNVS_LPSR  after init 0x40000008
[INFO]   B.1. Verify that ZMK_HWP bit is not set - using SNVS_LPMKCR[ZMK_HWP]
[INFO]           SNVS_LPMKCR before check ZMK_HWP 0xa
[INFO]           SNVS_LPMKCR[ZMK_HWP] Zeroizable Master Key hardware Programming mode is not set.
[INFO]   B.2. Verify that ZMK is not locked for write - using SNVS_HPLR[ZMK_WSL], SNVS_LPLR[ZMK_WHL,MKS_HL,ZMK_RHL]
[INFO]           SNVS_HPLR  before checking ZMK_WSL is 0x0
[INFO]           SNVS_HPLR[ZMK_WSL] Zeroizable Master Key Write Soft Lock is not set.
[INFO]           SNVS_LPLR  before checking ZMK_WHL,MKS_HL,ZMK_RHL is 0x0
[INFO]           SNVS_LPLR[ZMK_WHL] Zeroizable Master Key Write Soft Lock is not set.
[INFO]           SNVS_LPLR[MKS_HL] Master Key Select Hard Lock is not set.
[INFO]           SNVS_LPLR[ZMK_RHL] Zeroizable Master Key Read Hard Lock is not set.
[INFO]   B.3. Write key value to the ZMK registers. Full details in chapter 6.10.28
[INFO]           The ZMK key value before writing with 0x11223344 is 0x11223344
[INFO]   B.4. Verify that the correct key value is written.
[SUCCESS]                The new ZMK key value is = 0x11223344 and matches with the user desired value.
[INFO]   B.5. Set SNVS_LPMKCR[ZMK_VAL] bit if the ZMK (or the ZMK XORed with the OTPMK) will be used by CAAM as the master key.
[INFO]           SNVS_LPMKCR  before init 0xa
[INFO]           SNVS_LPMKCR  after init 0xa
[INFO]   B.9. Set SNVS_LPMKCR[MASTER_KEY_SEL] and SNVS_HPCOMR[MKS_EN] bits to select combination of OTPMK and ZMK to be provided to the hardware cryptographic module.
[INFO]           For our example MASTER_KEY_SEL is set as 10 - Select zeroizable master key when MKS_EN bit is set.
[INFO]           SNVS_LPMKCR  after init 0xa
[INFO]           SNVS_HPCOMR  before init 0x80002100
[INFO]           SNVS_HPCOMR  after init 0x80002100


