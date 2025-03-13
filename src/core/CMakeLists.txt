SET(defines "")
IF(MSVC)
    LIST(APPEND defines _CRT_SECURE_NO_WARNINGS)
ENDIF()

ADD_TARGET(
        MODE INTERFACE
        INC
        "${PROJECT_SOURCE_DIR}/include"
        DEFINE
        RAPIDJSON_HAS_STDSTRING
        ${defines}
)