NAME=r_cmd
OBJ=cmd.o plugin.o macro.o
DEPS=r_util r_lib r_cons

include ../config.mk

CFLAGS+=-DCORELIB

foo:
	for a in ${LIBSO} ${LIBAR} plugins ; do ${MAKE} $$a ; done

include ${STATIC_CMD_PLUGINS}
STATIC_OBJS=$(subst ..,p/..,$(subst cmd_,p/cmd_,$(STATIC_OBJ)))
OBJ+=${STATIC_OBJS}

plugins:
	cd p && ${MAKE} all

include ../rules.mk
