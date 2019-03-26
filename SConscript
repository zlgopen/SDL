import os   
import platform
CPPPATH=[]
sources=[]
env=DefaultEnvironment().Clone()
OS_NAME=platform.system()
LIB_DIR=os.environ['LIB_DIR'];
if OS_NAME == 'Windows':
	CPPPATH=['include','src']
	sources=Glob('src/atomic/*.c')+\
		Glob('src/audio/directsound/*.c')+\
		Glob('src/audio/disk/*.c')+\
		Glob('src/audio/dummy/*.c')+\
		Glob('src/audio/*.c')+\
		Glob('src/audio/winmm/*.c')+\
		Glob('src/audio/wasapi/*.c')+\
		Glob('src/core/windows/*.c')+\
		Glob('src/cpuinfo/*.c')+\
		Glob('src/events/*.c')+\
		Glob('src/file/*.c')+\
		Glob('src/filesystem/windows/*.c')+\
		Glob('src/libm/*.c')+\
		Glob('src/loadso/windows/*.c')+\
		Glob('src/power/*.c')+\
		Glob('src/power/windows/*.c')+\
		Glob('src/render/direct3d/*.c')+\
		Glob('src/render/direct3d11/*.c')+\
		Glob('src/render/opengl/*.c')+\
		Glob('src/render/opengles2/*.c')+\
		Glob('src/render/software/*.c')+\
		Glob('src/render/*.c')+\
		Glob('src/stdlib/*.c')+\
		Glob('src/thread/generic/SDL_syscond.c')+\
		Glob('src/thread/SDL_thread.c')+\
		Glob('src/thread/windows/*.c')+\
		Glob('src/timer/SDL_timer.c')+\
		Glob('src/timer/windows/*.c')+\
		Glob('src/video/dummy/*.c')+\
		Glob('src/video/windows/*.c')+\
		Glob('src/video/*.c')+\
		Glob('src/video/yuv2rgb/*.c')+\
		Glob('src/*.c')
		
elif OS_NAME == 'Linux':
	CPPPATH=[
		'/usr/include/gtk-3.0',
    	'/usr/include/dbus-1.0',
    	'/usr/lib/x86_64-linux-gnu/dbus-1.0/include',
	    '/usr/include/gio-unix-2.0/',
	    '/usr/include/pango-1.0',
	    '/usr/include/atk-1.0',
	    '/usr/include/cairo',
	    '/usr/include/pixman-1',
	    '/usr/include/gdk-pixbuf-2.0',
	    '/usr/include/glib-2.0',
		'/usr/lib/glib-2.0/include',
	    '/usr/lib/x86_64-linux-gnu/glib-2.0/include',
	    '/usr/include/ibus-1.0',
		'include',
		'gen',
		'src/video/khronos',
		'src'
		]
	sources=Glob('gen/*.c')+\
	Glob("src/*.c")+\
	Glob('src/atomic/*.c')+\
	Glob('src/audio/*.c')+\
	Glob('src/cpuinfo/*.c')+\
	Glob('src/events/*.c')+\
	Glob('src/file/*.c')+\
	Glob('src/libm/*.c')+\
	Glob('src/power/*.c')+\
	Glob('src/render/opengl/*.c')+\
	Glob('src/render/opengles2/*.c')+\
	Glob('src/render/software/*.c')+\
	Glob('src/render/*.c')+\
	Glob('src/stdlib/*.c')+\
	Glob('src/thread/*.c')+\
	Glob('src/timer/SDL_timer.c')+\
	Glob('src/video/yuv2rgb/*.c')+\
	Glob('src/video/*.c')+\
	Glob('src/loadso/dlopen//*.c')+\
	Glob('src/audio/dummy/*.c')+\
	Glob('src/audio/sndio/*.c')+\
	Glob('src/video/x11/*.c')+\
	Glob('src/video/dummy/*.c')+\
	Glob('src/core/linux/*.c')+\
	Glob('src/thread/pthread/*.c')+\
	Glob('src/power/linux/*.c')+\
	Glob('src/filesystem/unix/*.c')+\
	Glob('src/timer/unix/*.c')+\
	Glob('src/core/unix/*.c')+\
	Glob('src/main/dummy/*.c')

CCFLAGS=os.environ['CCFLAGS'];
CCFLAGS = CCFLAGS + ' -DSDL_STATIC_LIB -D__FLTUSED__ '
env.Library(os.path.join(LIB_DIR, 'SDL2'), sources, CPPPATH = CPPPATH, CCFLAGS = CCFLAGS)

