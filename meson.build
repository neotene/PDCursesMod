project('PDCurses', 'c', version : '0.1')

pdcurses_incdir = include_directories('.', is_system : true)
pdcurses_libsources = files(
  'wincon/pdcclip.c',
  'wincon/pdcdisp.c',
  'wincon/pdcgetsc.c',
  'wincon/pdckbd.c',
  'wincon/pdcscrn.c',
  'wincon/pdcsetsc.c',
  'wincon/pdcutil.c',

  'pdcurses/addch.c',
  'pdcurses/addchstr.c',
  'pdcurses/addstr.c',
  'pdcurses/attr.c',
  'pdcurses/beep.c',
  'pdcurses/bkgd.c',
  'pdcurses/border.c',
  'pdcurses/clear.c',
  'pdcurses/color.c',
  'pdcurses/debug.c',
  'pdcurses/delch.c',
  'pdcurses/deleteln.c',
  'pdcurses/getch.c',
  'pdcurses/getstr.c',
  'pdcurses/getyx.c',
  'pdcurses/inch.c',
  'pdcurses/inchstr.c',
  'pdcurses/initscr.c',
  'pdcurses/inopts.c',
  'pdcurses/insch.c',
  'pdcurses/insstr.c',
  'pdcurses/instr.c',
  'pdcurses/kernel.c',
  'pdcurses/keyname.c',
  'pdcurses/mouse.c',
  'pdcurses/move.c',
  'pdcurses/outopts.c',
  'pdcurses/overlay.c',
  'pdcurses/pad.c',
  'pdcurses/panel.c',
  'pdcurses/printw.c',
  'pdcurses/refresh.c',
  'pdcurses/scanw.c',
  'pdcurses/scr_dump.c',
  'pdcurses/scroll.c',
  'pdcurses/slk.c',
  'pdcurses/termattr.c',
  'pdcurses/touch.c',
  'pdcurses/util.c',
  'pdcurses/window.c',
)


c_args = ['-DPDC_WIDE', '-DPDC_FORCE_UTF8', '-DPDC_RGB']

libtype = get_option('default_library')

if libtype != 'static'
    c_args += ['-DPDC_DLL_BUILD']
endif

pdcurses_library = library(
  'pdcurses',
  pdcurses_libsources,
  include_directories: pdcurses_incdir,
  c_args: c_args,
)

pdcurses_dep = declare_dependency(
  link_with: pdcurses_library,
  include_directories: pdcurses_incdir,
)
