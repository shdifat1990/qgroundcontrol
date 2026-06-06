# ============================================================================
# Swarm Module - Multi-vehicle UAV control QML plugin
# ============================================================================

qt_add_qml_module(SwarmModule
    URI Swarm
    VERSION 1.0
    RESOURCE_PREFIX /qml/Swarm
    QML_FILES
        QmlControls/qmldir
        QmlControls/SwarmDashboard.qml
        QmlControls/SwarmControlPanel.qml
        QmlControls/SwarmFormationSelector.qml
        QmlControls/SwarmHealthIndicator.qml
        QmlControls/SwarmInterface.qml
        QmlControls/SwarmMapVisualization.qml
        QmlControls/SwarmMiniMap.qml
        QmlControls/SwarmTelemetryWidget.qml
        QmlControls/SwarmVehicleList.qml
        QmlControls/SwarmVehicleStatus.qml
        QmlControls/SwarmAlertSystem.qml
    NO_PLUGIN
)