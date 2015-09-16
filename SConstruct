def expandPath(path):
	return Dir(path).get_abspath() + "/"

libsPath = [expandPath("libs")]
includePath = [expandPath("src/headers"), expandPath("include/godot"), expandPath("include/godot/core")]
buildPath = [Dir("build").get_abspath() + "/"]

libs = ["core.x11.tools.64"]
src_files = Glob("src/*.cpp")

env = Environment(LIBS=libs, CPPPATH=includePath, LIBPATH=libsPath)
env.Program("heightmap", src_files)

