## Source directory

SUBDIRS =

AM_CFLAGS = -I$(top_srcdir) $(GLIB_CFLAGS)
AM_CFLAGS += -Wall -Wextra

if DEBUG
AM_CFLAGS += -Werror
AM_CFLAGS += -Wno-missing-field-initializers -Wno-unused-parameter
endif

AM_LDFLAGS = -L$(top_builddir)/libvmi/.libs/
LDADD = -lvmi -lm $(LIBS) $(GLIB_LIBS)

bin_PROGRAMS = vmi-process-list \
               vmi-module-list \
               vmi-dump-memory

if WINDOWS
bin_PROGRAMS += vmi-win-guid \
                vmi-win-offsets
endif

noinst_PROGRAMS = map-symbol \
                  map-addr \
                  event-example \
                  msr-event-example \
                  singlestep-event-example \
                  interrupt-event-example \
                  step-event-example \
                  va-pages \
                  xen-emulate-response

vmi_process_list_SOURCES = process-list.c
vmi_module_list_SOURCES = module-list.c
vmi_dump_memory_SOURCES = dump-memory.c
vmi_win_guid_SOURCES = win-guid.c win-guid.h
vmi_win_offsets_SOURCES = win-offsets.c

map_symbol_SOURCES = map-symbol.c
map_addr_SOURCES = map-addr.c
event_example_SOURCES = event-example.c
msr_event_example_SOURCES = msr-event-example.c
singlestep_event_example_SOURCES = singlestep-event-example.c
interrupt_event_example_SOURCES = interrupt-event-example.c
step_event_example_SOURCES = step-event-example.c
va_pages_SOURCES = va-pages.c
xen_emulate_response_SOURCES = xen-emulate-response.c
