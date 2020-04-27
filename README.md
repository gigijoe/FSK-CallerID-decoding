forked from jeniljain29392/FSK-CallerID-decoding

@ More IIR coef for sample rate 8k / 12k / 24k
@ 8k sample rate FSK decode fail

# FSK-CallerID-decoding

Caller ID  is a telephone service, that transmits a caller's number to the called party's telephone equipment
during the ringing signal. Modulation technique used for transmittinf Caller ID is either FSK or DTMF.
FSK CallerID Decoding, demodulatess and decode the caller ID signal coming from the telephone jack and gives
the Caller ID message. 

Folder Structure
- include         : includes the libraries used and the header files
- gnuplot         : includes libraries for ploting the FSK signals
- Doxygen         : Doxygen documentation of the APIs
- audacity_files  : caller ID signals used for decoding the message
- fskmodem.c      : demodulated the FSK caller ID signals
- ciddeco.c       : Decodes the Caller ID message from the demodulated signal
- Makefile        : makefile to compile and run the program.
  
# Compile and run

$ make wavfile
$ sox audacity_files/CID-4_48X.wav -r 12000 audacity_files/CID-4_12X.wav
$ ./cid_fsk ./audacity_files/CID-4_12X.wav
	Press ctrl-c


