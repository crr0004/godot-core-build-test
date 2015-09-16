#Getting Setup
1. Compile godot
2. Link against libcore.x11.tools.64
3. Include header search path that contains all the core headers. This must include all the headers inside the core folder as well the core folder itself (See notes 1). You must also include your relevant platform_config.h header (See notes 2).
4. 


#Notes
1. Some the headers inside the core itself reference the headers through the path of "core/*.h" which makes no sense. The file that gave the error for this was core/os/memory_pool_static.h"
2. core/typedefs.h uses the platform_config.h file. If you're not going to develop/run your code on multiple platforms than you can use the one built inside godot
