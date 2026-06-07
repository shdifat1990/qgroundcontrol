qt_add_library(FirstRunPromptDialogsModule STATIC)

qt_add_qml_module(FirstRunPromptDialogsModule
    URI QGroundControl.FirstRunPromptDialogs
    VERSION 1.0
    RESOURCE_PREFIX /qml
    QML_FILES
        FirstRunPrompt.qml
        InitialSetupPrompt.qml
    NO_PLUGIN
)


# Link Qt libraries to ensure qmlcache is properly initialized for static library
target_link_libraries(FirstRunPromptDialogsModule
    PUBLIC
        Qt6::Core
        Qt6::Qml
        Qt6::QmlIntegration
)

# Force-link the module so its qmlcache initialization
# is included in the final executable (NO_PLUGIN, so no plugin library)
target_link_libraries(${CMAKE_PROJECT_NAME} PRIVATE FirstRunPromptDialogsModule)

