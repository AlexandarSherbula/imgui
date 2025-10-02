project(imgui)

set(IMGUI_SRC
	"imconfig.h"
	"imgui.h"
	"imgui.cpp"
	"imgui_draw.cpp"
	"imgui_tables.cpp"
	"imgui_internal.h"
	"imgui_widgets.cpp"
	"imstb_rectpack.h"
	"imstb_textedit.h"
	"imstb_truetype.h"
	"imgui_demo.cpp"
)

add_library(imgui STATIC ${IMGUI_SRC})
target_compile_features(Engine PRIVATE cxx_std_20)
target_include_directories(imgui PUBLIC ${CMAKE_SOURCE_DIR}/Engine/vendor/imgui/)
