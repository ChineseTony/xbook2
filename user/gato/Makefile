X_LIBS		:= libxlibc-0.0.1.a libpthread-0.0.1.a libgapi-0.1.0.a libpng-1.6.37.a libzlib-1.2.11.a libjpeg-9d.a
X_LIBS		+= libgato-0.0.1.a

X_CFLAGS	:= -fno-builtin -fno-PIE -m32 -fno-stack-protector -std=gnu99 -O3 -g

NAME		:= gato

SRC			+= main.c

define CUSTOM_TARGET_CMD
echo [APP] $@; \
$(LD) $(X_LDFLAGS) $(X_OBJS) -o $@ $(patsubst %, -L%, $(X_LIBDIRS)) --start-group $(patsubst %, -l:%, $(X_LIBS)) --end-group; \
cp $@ $(srctree)/../develop/rom/usr
endef
