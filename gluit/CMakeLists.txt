add_library(glui
        glui.cc
		glui_add_controls.cc
		glui_algebra3.cc
		glui_arcball.cc
		glui_bitmap_img_data.cc
		glui_bitmaps.cc
		glui_button.cc
		glui_checkbox.cc
		glui_column.cc
		glui_control.cc
		glui_edittext.cc
		glui_listbox.cc
		glui_mouse_iaction.cc
		glui_node.cc
		glui_panel.cc
		glui_quaternion.cc
		glui_radio.cc
		glui_rollout.cc
		glui_rotation.cc
		glui_separator.cc
		glui_slider.cc
		glui_spinner.cc
		glui_statictext.cc
		glui_translation.cc)

target_include_directories(glui PRIVATE
	${CMAKE_SOURCE_DIR}/include
    INTERFACE
    ${CMAKE_INSTALL_INCLUDE_DIR})

set(INSTALL_CONFIGDIR ${CMAKE_INSTALL_LIBDIR}/cmake/glui)
install(TARGETS glui
        EXPORT GluiTargets
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDE_DIR}
)

install(EXPORT GluiTargets
    FILE GluiConfig.cmake
    NAMESPACE Glui::
    DESTINATION ${INSTALL_CONFIGDIR}
)
