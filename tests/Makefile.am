AM_CFLAGS = \
    $(GNOME_POMODORO_CFLAGS) \
    $(WARNING_CFLAGS)

noinst_PROGRAMS = \
    tests

tests_SOURCES = \
    tests.vala \
    test-timer.vala \
    ../lib/gnome-pomodoro.vapi


tests_DEPENDENCIES = \
    ../lib/libgnome-pomodoro.la

tests_VALAFLAGS = \
    --vapidir=$(top_builddir)/vapi \
    --pkg config \
    --pkg gobject-2.0 \
    --pkg gio-2.0 \
    --pkg gdk-3.0 \
    --pkg gtk+-3.0 \
    --pkg posix

tests_CPPFLAGS = \
    $(GNOME_POMODORO_CFLAGS) \
    $(WARNING_CFLAGS)

tests_LDADD = \
    $(GNOME_POMODORO_LIBS) \
    $(top_builddir)/lib/libgnome-pomodoro.la


test: tests
	$(builddir)/$<

# run make test as part of make check
check-local: test

.PHONY: test

-include $(top_srcdir)/git.mk
