# ============================================================================
# Swarm Manager Module
# ============================================================================

# Swarm module is integrated directly into the main QGC executable
# to ensure proper linking with Vehicle and other core modules.

# Note: Swarm QML files are loaded at runtime, no separate library needed.
# The SwarmManager class is included via src/CMakeLists.txt target_sources.

# Always include Swarm resources to enable the import path
target_sources(${CMAKE_PROJECT_NAME}
    PRIVATE
        Swarm/Swarm.qrc
)