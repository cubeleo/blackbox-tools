add_library(blackbox_common STATIC
    parser.c tools.c platform.c stream.c decoders.c units.c blackbox_fielddefs.c
)

add_executable(blackbox_decode
    blackbox_decode.c gpxwriter.c imu.c battery.c stats.c
)
target_link_libraries(blackbox_decode blackbox_common m pthread)
