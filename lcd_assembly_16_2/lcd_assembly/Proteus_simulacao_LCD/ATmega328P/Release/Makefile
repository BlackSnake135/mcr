###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = ATmega328P
COMPILER = "AVRASM (Proteus)"
TARGET = Release
SHELL = C:\Windows\system32\cmd.exe

## Tools general options
ASMFLAGS=-fI -i"C:\Program Files (x86)\Proteus 8 Professional\Tools\AVRASM\appnotes\m328Pdef.inc"

## Processing Tools
ASM=avrasm2.exe
#  C:/Thiago Ribeiro/Fatec/Microcontroladores/Exemplo9/exemplo9/ATmega328P/Release/Release.hex: TOOL=ASM
#     C:/Thiago Ribeiro/Fatec/Microcontroladores/Exemplo9/exemplo9/ATmega328P/main.asm

# Build tree:
all:	Release

Release:	Release.hex
	cp "Release.hex" "../../ATmega328P.hex"

Release.hex:	../main.asm 
	$(ASM) $(ASMFLAGS)  -o "Release.hex" -l Release.lst "..\main.asm"

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Release.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Release.hex

