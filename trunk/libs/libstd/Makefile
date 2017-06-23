

all: libgcc_s.so.1 libstdc++.so.6
	echo install std library to ${ROMFSDIR}
	rm -f ${ROMFSDIR}/usr/lib/libgcc_s.so.1
	rm -f ${ROMFSDIR}/usr/lib/libstdc++.so.6
	rm -f ${ROMFSDIR}/usr/share/libgcc_s.so.1
	rm -f ${ROMFSDIR}/usr/share/libstdc++.so.6
#	ls -la ${ROMFSDIR}/lib/libgcc_s.so.1 ${ROMFSDIR}/lib/libstdc++.so.6

config_test:
	echo "test std library";

configure:
	echo configure ${ROMFSDIR}

clean:
	echo clean ${ROMFSDIR}/lib/libgcc_s.so.1

install:
	echo install

romfs:
#	$(ROMFSINST) libgcc_s.so.1 /lib/libgcc_s.so.1
#	$(ROMFSINST) libstdc++.so.6 /lib/libstdc++.so.6
#	$(ROMFSINST) libgcc_s.so.1 /usr/share/libgcc_s.so.1
#	$(ROMFSINST) libstdc++.so.6 /usr/share/libstdc++.so.6
#	$(ROMFSINST) -s /usr/share/libgcc_s.so.1 /usr/share/libgcc_s.so
#	$(ROMFSINST) -s /usr/share/libstdc++.so.6 /usr/share/libstdc++.so
#	$(ROMFSINST) libgcc_s.so.1 /usr/lib/libgcc_s.so.1
#	$(ROMFSINST) libstdc++.so.6 /usr/lib/libstdc++.so.6
#	$(ROMFSINST) -s /usr/lib/libgcc_s.so.1 /usr/lib/libgcc_s.so
#	$(ROMFSINST) -s /usr/lib/libstdc++.so.6 /usr/lib/libstdc++.so
#	cp -f libgcc_s.so.1 ${ROMFSDIR}/usr/lib/libgcc_s.so.1
#	cp -f libstdc++.so.6 ${ROMFSDIR}/usr/lib/libstdc++.so.6
#	ls -la ../../romfs/usr/lib/libgcc_s.so.1 ../../romfs/usr/lib/libstdc++.so.6
	mkdir -p ${ROMFSDIR}/usr/share/
	cp -f libgcc_s.so.1 ${ROMFSDIR}/usr/share/libgcc_s.so.1
	cp -f libstdc++.so.6 ${ROMFSDIR}/usr/share/libstdc++.so.6
#	ls -la ../../romfs/usr/share/libgcc_s.so.1 ../../romfs/usr/share/libstdc++.so.6
#	if [ ! -L "${ROMFSDIR}/usr/share/libgcc_s.so" ]; then
		cd ${ROMFSDIR}/usr/share/;
		ln -f -s libgcc_s.so.1 libgcc_s.so;
#	fi
#	if [ ! -L "${ROMFSDIR}/usr/share/libstdc++.so" ]; then
		cd ${ROMFSDIR}/usr/share/;
		ln -f -s libstdc++.so.6 libstdc++.so;
#	fi
	mkdir -p ${ROMFSDIR}/usr/share/bkye/
	$(ROMFSINST) -s /usr/share/libgcc_s.so.1 /usr/share/bkye/libgcc_s.so
	$(ROMFSINST) -s /usr/share/libgcc_s.so.1 /usr/share/bkye/libgcc_s.so.1
	$(ROMFSINST) -s /usr/share/libstdc++.so.6 /usr/share/bkye/libstdc++.so
	$(ROMFSINST) -s /usr/share/libstdc++.so.6 /usr/share/bkye/libstdc++.so.6
	$(ROMFSINST) -s /usr/share/libgcc_s.so.1 /lib/libgcc_s.so.1
	$(ROMFSINST) -s /usr/share/libstdc++.so.6 /lib/libstdc++.so.6

