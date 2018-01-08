

top_srcdir		?= ..

include $(top_srcdir)/include/mk/env_pre.mk

# XXX (garrcoop):
# 1. kdump shouldn't be compiled by default, because it's runtime based and
#    WILL crash the build host (the tests need to be fixed to just build, not
#    run).
FILTER_OUT_DIRS		:= kdump

ifneq ($(WITH_OPEN_POSIX_TESTSUITE),yes)
FILTER_OUT_DIRS		+= open_posix_testsuite
endif

ifneq ($(WITH_REALTIME_TESTSUITE),yes)
FILTER_OUT_DIRS		+= realtime
endif

include $(top_srcdir)/include/mk/generic_trunk_target.mk
