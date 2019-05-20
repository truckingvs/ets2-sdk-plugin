SDK_HEADERS=\
	../../include/*.h \
	../../include/common/*.h \
	../../include/amtrucks/*.h \
	../../include/eurotrucks2/*.h

SDK_INCLUDES=\
	-I../../include \
	-I../../include/common/ \
	-I../../include/amtrucks/ \
	-I../../include/eurotrucks2

telemetry_position.so:  *.cpp $(SDK_HEADERS)
	gcc -o $@ -fPIC -Wall --shared -Wl,-soname,$@ $(SDK_INCLUDES) *.cpp

.PHONY: clean
clean:
	@rm -f -- *.so
