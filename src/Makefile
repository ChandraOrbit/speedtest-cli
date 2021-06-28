# This Makefile for MIPSEL 24kc proc
TOOLCHAIN_DIR=/usr/path/openwrt/staging_dir/toolchain-mipsel_24kc_gcc-7.5.0_musl
INCLUDE_DIR=$(TOOLCHAIN_DIR)/usr/include
CC=mipsel-openwrt-linux-gcc
LDFLAGS=-lpthread -lcurl -lexpat -lm
speedtest: speedtest.o
	$(CC) $(LDFLAGS) speedtest.o -o speedtest

speedtest.o: speedtest.c
	$(CC) $(CFLAGS) -c speedtest.c

# remove object files and executable when user executes "make clean"
clean:
	rm *.o speedtest
