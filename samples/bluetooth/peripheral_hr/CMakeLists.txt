include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(NONE)

FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE
  ${app_sources}
  ../gatt/hrs.c
  ../gatt/dis.c
  ../gatt/bas.c
  )

zephyr_library_include_directories($ENV{ZEPHYR_BASE}/samples/bluetooth)
