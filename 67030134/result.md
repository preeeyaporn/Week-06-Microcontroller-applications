```C
LAB 6-1
``` 

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c87de4e3-6a3e-4c04-952a-217d5beb0c9d" />

```C


``` 

```C
Executing action: size-components
Running ninja in directory /project/lab6_1_basic_build/build
Executing "ninja all"...
[1/4] cd /project/lab6_1_basic_build/build/esp-idf/esptool_py && /opt/esp/python_env/idf6.0_py3.12_env/bin/python /opt/esp/idf/components/partition_table/check_sizes.py --offset 0x8000 partition --type app /project/lab6_1_basic_build/build/partition_table/partition-table.bin /project/lab6_1_basic_build/build/lab6_1_basic_build.bin
lab6_1_basic_build.bin binary size 0x279c0 bytes. Smallest app partition is 0x100000 bytes. 0xd8640 bytes (85%) free.
[2/4] Performing build step for 'bootloader'
[1/1] cd /project/lab6_1_basic_build/build/bootloader/esp-idf/esptool_py && /opt/esp/python_env/idf6.0_py3.12_env/bin/python /opt/esp/idf/components/partition_table/check_sizes.py --offset 0x8000 bootloader 0x1000 /project/lab6_1_basic_build/build/bootloader/bootloader.bin
Bootloader binary size 0x66a0 bytes. 0x960 bytes (8%) free.
[3/4] No install step for 'bootloader'
[4/4] Completed 'bootloader'
Running ninja in directory /project/lab6_1_basic_build/build
Executing "ninja size-components"...
[0/1] cd /project/lab6_1_basic_build/build && /opt/esp/tools/cmake/3.30.2/bin/cmake -D "IDF_SIZE_TOOL=/opt/esp/python_env/idf6.0_py3.12_env/bin/python;-m;esp_idf_size" -D IDF_SIZE_MODE=--archives -D MAP_FILE=/project/lab6_1_basic_build/build/lab6_1_basic_build.map -D OUTPUT_JSON= -P /opt/esp/idf/tools/cmake/run_size_tool.cmake
                                                                                  Per-archive contributions to ELF file                                                                                  
┏━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━┳━━━━━━┳━━━━━━━┳━━━━━━━┳━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━┓
┃ Archive File            ┃ Total Size ┃ DRAM ┃ .bss ┃ .data ┃  IRAM ┃ .text ┃ .vectors ┃ Flash Code ┃ .text ┃ Flash Data ┃ .rodata ┃ .appdesc ┃ RTC FAST ┃ .force_fast ┃ RTC SLOW ┃ .rtc_slow_reserved ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━╇━━━━━━╇━━━━━━━╇━━━━━━━╇━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━┩
│ libesp_app_format.a     │      26474 │   10 │   10 │     0 │     0 │     0 │        0 │        417 │   417 │      26047 │   25791 │      256 │        0 │           0 │        0 │                  0 │
│ libc.a                  │      23792 │  572 │  312 │   260 │     0 │     0 │        0 │      21560 │ 21560 │       1660 │    1660 │        0 │        0 │           0 │        0 │                  0 │
│ libfreertos.a           │      18052 │ 3847 │  741 │  3106 │ 12882 │ 12882 │        0 │        367 │   367 │        956 │     956 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_hw_support.a     │      13719 │  382 │   76 │   306 │  6019 │  6019 │        0 │       6356 │  6356 │        902 │     902 │        0 │       36 │          36 │       24 │                 24 │
│ libesp_system.a         │      12611 │  742 │  309 │   433 │  3570 │  3570 │        0 │       7661 │  7661 │        638 │     638 │        0 │        0 │           0 │        0 │                  0 │
│ libheap.a               │      12037 │   12 │    8 │     4 │  7340 │  7340 │        0 │       3095 │  3095 │       1590 │    1590 │        0 │        0 │           0 │        0 │                  0 │
│ libhal.a                │      10656 │ 2621 │    8 │  2613 │  5893 │  5893 │        0 │       2044 │  2044 │         98 │      98 │        0 │        0 │           0 │        0 │                  0 │
│ libspi_flash.a          │       9845 │ 1140 │   24 │  1116 │  7194 │  7194 │        0 │       1082 │  1082 │        429 │     429 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_driver_uart.a    │       7752 │  336 │   32 │   304 │     0 │     0 │        0 │       6815 │  6815 │        601 │     601 │        0 │        0 │           0 │        0 │                  0 │
│ libvfs.a                │       4294 │  236 │   44 │   192 │     0 │     0 │        0 │       3915 │  3915 │        143 │     143 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_mm.a             │       4109 │  164 │  128 │    36 │  1062 │  1062 │        0 │       2669 │  2669 │        214 │     214 │        0 │        0 │           0 │        0 │                  0 │
│ libxtensa.a             │       3413 │ 1044 │    0 │  1044 │  2216 │  1789 │      427 │        117 │   117 │         36 │      36 │        0 │        0 │           0 │        0 │                  0 │
│ libnewlib.a             │       3144 │  360 │  200 │   160 │  1473 │  1473 │        0 │       1202 │  1202 │        109 │     109 │        0 │        0 │           0 │        0 │                  0 │
│ libbootloader_support.a │       2189 │    0 │    0 │     0 │  2055 │  2055 │        0 │         94 │    94 │         40 │      40 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_common.a         │       1841 │    0 │    0 │     0 │     0 │     0 │        0 │         51 │    51 │       1790 │    1790 │        0 │        0 │           0 │        0 │                  0 │
│ libsoc.a                │       1521 │   40 │    0 │    40 │    37 │    37 │        0 │          0 │     0 │       1444 │    1444 │        0 │        0 │           0 │        0 │                  0 │
│ liblog.a                │       1258 │  284 │  276 │     8 │   329 │   329 │        0 │        621 │   621 │         24 │      24 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_ringbuf.a        │       1150 │    0 │    0 │     0 │  1053 │  1053 │        0 │          0 │     0 │         97 │      97 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_partition.a      │       1035 │    8 │    8 │     0 │     0 │     0 │        0 │        990 │   990 │         37 │      37 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_rom.a            │        801 │    0 │    0 │     0 │   245 │   245 │        0 │          0 │     0 │        556 │     556 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_vfs_console.a    │        677 │   16 │   16 │     0 │     0 │     0 │        0 │        481 │   481 │        180 │     180 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_timer.a          │        536 │    8 │    8 │     0 │   145 │   145 │        0 │        375 │   375 │          8 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ libxt_hal.a             │        475 │    0 │    0 │     0 │   443 │   443 │        0 │          0 │     0 │         32 │      32 │        0 │        0 │           0 │        0 │                  0 │
│ libefuse.a              │        319 │    0 │    0 │     0 │     0 │     0 │        0 │        263 │   263 │         56 │      56 │        0 │        0 │           0 │        0 │                  0 │
│ libapp_update.a         │        183 │    4 │    4 │     0 │     0 │     0 │        0 │        149 │   149 │         30 │      30 │        0 │        0 │           0 │        0 │                  0 │
│ libmain.a               │        126 │    0 │    0 │     0 │     0 │     0 │        0 │        126 │   126 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libpthread.a            │         25 │    0 │    0 │     0 │     0 │     0 │        0 │         25 │    25 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_security.a       │         20 │    0 │    0 │     0 │     0 │     0 │        0 │         12 │    12 │          8 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ libcxx.a                │         10 │    0 │    0 │     0 │     0 │     0 │        0 │         10 │    10 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libnvs_sec_provider.a   │          5 │    0 │    0 │     0 │     0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libesp_phy.a            │          5 │    0 │    0 │     0 │     0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
└─────────────────────────┴────────────┴──────┴──────┴───────┴───────┴───────┴──────────┴────────────┴───────┴────────────┴─────────┴──────────┴──────────┴─────────────┴──────────┴────────────────────┘
```
```c
Executing action: size-files
Running ninja in directory /project/lab6_1_basic_build/build
Executing "ninja all"...
[1/4] cd /project/lab6_1_basic_build/build/esp-idf/esptool_py && /opt/esp/python_env/idf6.0_py3.12_env/bin/python /opt/esp/idf/components/partition_table/check_sizes.py --offset 0x8000 partition --type app /project/lab6_1_basic_build/build/partition_table/partition-table.bin /project/lab6_1_basic_build/build/lab6_1_basic_build.bin
lab6_1_basic_build.bin binary size 0x279c0 bytes. Smallest app partition is 0x100000 bytes. 0xd8640 bytes (85%) free.
[2/4] Performing build step for 'bootloader'
[1/1] cd /project/lab6_1_basic_build/build/bootloader/esp-idf/esptool_py && /opt/esp/python_env/idf6.0_py3.12_env/bin/python /opt/esp/idf/components/partition_table/check_sizes.py --offset 0x8000 bootloader 0x1000 /project/lab6_1_basic_build/build/bootloader/bootloader.bin
Bootloader binary size 0x66a0 bytes. 0x960 bytes (8%) free.
[3/4] No install step for 'bootloader'
[4/4] Completed 'bootloader'
Running ninja in directory /project/lab6_1_basic_build/build
Executing "ninja size-files"...
[0/1] cd /project/lab6_1_basic_build/build && /opt/esp/tools/cmake/3.30.2/bin/cmake -D "IDF_SIZE_TOOL=/opt/esp/python_env/idf6.0_py3.12_env/bin/python;-m;esp_idf_size" -D IDF_SIZE_MODE=--files -D MAP_FILE=/project/lab6_1_basic_build/build/lab6_1_basic_build.map -D OUTPUT_JSON= -P /opt/esp/idf/tools/cmake/run_size_tool.cmake
                                                                                         Per-file contributions to ELF file                                                                                         
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━┳━━━━━━┳━━━━━━━┳━━━━━━┳━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━━┳━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━┓
┃ Object File                         ┃ Total Size ┃ DRAM ┃ .bss ┃ .data ┃ IRAM ┃ .text ┃ .vectors ┃ Flash Code ┃ .text ┃ Flash Data ┃ .rodata ┃ .appdesc ┃ RTC FAST ┃ .force_fast ┃ RTC SLOW ┃ .rtc_slow_reserved ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━╇━━━━━━╇━━━━━━━╇━━━━━━╇━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━━╇━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━┩
│ esp_app_desc.c.obj                  │      26474 │   10 │   10 │     0 │    0 │     0 │        0 │        417 │   417 │      26047 │   25791 │      256 │        0 │           0 │        0 │                  0 │
│ libc_a-vfprintf.o                   │      13396 │    0 │    0 │     0 │    0 │     0 │        0 │      12824 │ 12824 │        572 │     572 │        0 │        0 │           0 │        0 │                  0 │
│ tasks.c.obj                         │       9565 │  718 │  696 │    22 │ 8300 │  8300 │        0 │          0 │     0 │        547 │     547 │        0 │        0 │           0 │        0 │                  0 │
│ tlsf.c.obj                          │       6833 │    0 │    0 │     0 │ 5358 │  5358 │        0 │       1199 │  1199 │        276 │     276 │        0 │        0 │           0 │        0 │                  0 │
│ uart_vfs.c.obj                      │       4966 │  148 │   20 │   128 │    0 │     0 │        0 │       4469 │  4469 │        349 │     349 │        0 │        0 │           0 │        0 │                  0 │
│ port.c.obj                          │       4322 │ 3124 │   40 │  3084 │ 1124 │  1124 │        0 │          0 │     0 │         74 │      74 │        0 │        0 │           0 │        0 │                  0 │
│ wdt_hal_iram.c.obj                  │       3867 │ 2341 │    0 │  2341 │ 1526 │  1526 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_mmu_map.c.obj                   │       3720 │  132 │  128 │     4 │  777 │   777 │        0 │       2669 │  2669 │        142 │     142 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-dtoa.o                       │       3626 │    0 │    0 │     0 │    0 │     0 │        0 │       3626 │  3626 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ vfs.c.obj                           │       3416 │  232 │   40 │   192 │    0 │     0 │        0 │       3169 │  3169 │         15 │      15 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_generic.c.obj        │       3241 │  250 │    0 │   250 │ 2991 │  2991 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ rtc_clk.c.obj                       │       2857 │   78 │    4 │    74 │ 2779 │  2779 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ uart.c.obj                          │       2786 │  188 │   12 │   176 │    0 │     0 │        0 │       2346 │  2346 │        252 │     252 │        0 │        0 │           0 │        0 │                  0 │
│ intr_alloc.c.obj                    │       2628 │   30 │   22 │     8 │  583 │   583 │        0 │       1910 │  1910 │        105 │     105 │        0 │        0 │           0 │        0 │                  0 │
│ queue.c.obj                         │       2467 │    0 │    0 │     0 │ 2194 │  2194 │        0 │          0 │     0 │        273 │     273 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-mprec.o                      │       2260 │    0 │    0 │     0 │    0 │     0 │        0 │       2008 │  2008 │        252 │     252 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_hal_iram.c.obj            │       2101 │    0 │    0 │     0 │ 2101 │  2101 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ task_wdt.c.obj                      │       2034 │   38 │    5 │    33 │    0 │     0 │        0 │       1881 │  1881 │        115 │     115 │        0 │        0 │           0 │        0 │                  0 │
│ esp_err_to_name.c.obj               │       1841 │    0 │    0 │     0 │    0 │     0 │        0 │         51 │    51 │       1790 │    1790 │        0 │        0 │           0 │        0 │                  0 │
│ xtensa_vectors.S.obj                │       1801 │   20 │    0 │    20 │ 1745 │  1318 │      427 │          0 │     0 │         36 │      36 │        0 │        0 │           0 │        0 │                  0 │
│ mmu_hal.c.obj                       │       1607 │  206 │    0 │   206 │ 1401 │  1401 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ periph_ctrl.c.obj                   │       1597 │   42 │   34 │     8 │  107 │   107 │        0 │       1427 │  1427 │         21 │      21 │        0 │        0 │           0 │        0 │                  0 │
│ cpu_start.c.obj                     │       1450 │    5 │    5 │     0 │  658 │   658 │        0 │        779 │   779 │          8 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ rtc_time.c.obj                      │       1237 │    0 │    0 │     0 │ 1200 │  1200 │        0 │          0 │     0 │         37 │      37 │        0 │        0 │           0 │        0 │                  0 │
│ esp_flash_api.c.obj                 │       1172 │   30 │    0 │    30 │  946 │   946 │        0 │         16 │    16 │        180 │     180 │        0 │        0 │           0 │        0 │                  0 │
│ rtc_io_periph.c.obj                 │       1168 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │       1168 │    1168 │        0 │        0 │           0 │        0 │                  0 │
│ ringbuf.c.obj                       │       1150 │    0 │    0 │     0 │ 1053 │  1053 │        0 │          0 │     0 │         97 │      97 │        0 │        0 │           0 │        0 │                  0 │
│ heap_caps_base.c.obj                │       1115 │    0 │    0 │     0 │ 1053 │  1053 │        0 │          0 │     0 │         62 │      62 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_winbond.c.obj        │       1092 │  140 │    0 │   140 │  952 │   952 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ panic_arch.c.obj                    │       1091 │    0 │    0 │     0 │    0 │     0 │        0 │        803 │   803 │        288 │     288 │        0 │        0 │           0 │        0 │                  0 │
│ bootloader_flash.c.obj              │       1084 │    0 │    0 │     0 │ 1044 │  1044 │        0 │          0 │     0 │         40 │      40 │        0 │        0 │           0 │        0 │                  0 │
│ rtc_init.c.obj                      │       1083 │    0 │    0 │     0 │    0 │     0 │        0 │       1083 │  1083 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ xtensa_intr_asm.S.obj               │       1075 │ 1024 │    0 │  1024 │   51 │    51 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ bootloader_flash_config_esp32.c.obj │       1057 │    0 │    0 │     0 │  971 │   971 │        0 │         86 │    86 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ipc.c.obj                       │       1038 │  402 │   66 │   336 │  267 │   267 │        0 │        343 │   343 │         26 │      26 │        0 │        0 │           0 │        0 │                  0 │
│ locks.c.obj                         │       1019 │  176 │  168 │     8 │  613 │   613 │        0 │        137 │   137 │         93 │      93 │        0 │        0 │           0 │        0 │                  0 │
│ memory_layout.c.obj                 │       1016 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │       1016 │    1016 │        0 │        0 │           0 │        0 │                  0 │
│ cache_utils.c.obj                   │        980 │   18 │   14 │     4 │  734 │   734 │        0 │         81 │    81 │        147 │     147 │        0 │        0 │           0 │        0 │                  0 │
│ panic.c.obj                         │        968 │   25 │    5 │    20 │   30 │    30 │        0 │        897 │   897 │         16 │      16 │        0 │        0 │           0 │        0 │                  0 │
│ heap_caps_init.c.obj                │        961 │    4 │    4 │     0 │    0 │     0 │        0 │        900 │   900 │         57 │      57 │        0 │        0 │           0 │        0 │                  0 │
│ partition.c.obj                     │        889 │    8 │    8 │     0 │    0 │     0 │        0 │        844 │   844 │         37 │      37 │        0 │        0 │           0 │        0 │                  0 │
│ nullfs.c.obj                        │        878 │    4 │    4 │     0 │    0 │     0 │        0 │        746 │   746 │        128 │     128 │        0 │        0 │           0 │        0 │                  0 │
│ multi_heap.c.obj                    │        792 │    0 │    0 │     0 │  515 │   515 │        0 │        228 │   228 │         49 │      49 │        0 │        0 │           0 │        0 │                  0 │
│ clk.c.obj                           │        778 │    0 │    0 │     0 │    0 │     0 │        0 │        765 │   765 │         13 │      13 │        0 │        0 │           0 │        0 │                  0 │
│ log_binary_heap.c.obj               │        760 │  260 │  260 │     0 │    0 │     0 │        0 │        476 │   476 │         24 │      24 │        0 │        0 │           0 │        0 │                  0 │
│ heap_caps.c.obj                     │        744 │    8 │    4 │     4 │  414 │   414 │        0 │        219 │   219 │        103 │     103 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-fseeko.o                     │        718 │    0 │    0 │     0 │    0 │     0 │        0 │        718 │   718 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-fvwrite.o                    │        703 │    0 │    0 │     0 │    0 │     0 │        0 │        703 │   703 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_rom_gpio.c.obj                  │        686 │    0 │    0 │     0 │  130 │   130 │        0 │          0 │     0 │        556 │     556 │        0 │        0 │           0 │        0 │                  0 │
│ clk_tree_hal.c.obj                  │        679 │    0 │    0 │     0 │    0 │     0 │        0 │        621 │   621 │         58 │      58 │        0 │        0 │           0 │        0 │                  0 │
│ vfs_console.c.obj                   │        677 │   16 │   16 │     0 │    0 │     0 │        0 │        481 │   481 │        180 │     180 │        0 │        0 │           0 │        0 │                  0 │
│ portasm.S.obj                       │        638 │    0 │    0 │     0 │  638 │   638 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_cpu_intr.c.obj                  │        611 │    0 │    0 │     0 │    0 │     0 │        0 │         77 │    77 │        534 │     534 │        0 │        0 │           0 │        0 │                  0 │
│ time.c.obj                          │        585 │   20 │   20 │     0 │    0 │     0 │        0 │        565 │   565 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ memory_layout_utils.c.obj           │        576 │    0 │    0 │     0 │    0 │     0 │        0 │        549 │   549 │         27 │      27 │        0 │        0 │           0 │        0 │                  0 │
│ system_internal.c.obj               │        533 │    0 │    0 │     0 │  517 │   517 │        0 │          0 │     0 │         16 │      16 │        0 │        0 │           0 │        0 │                  0 │
│ panic_handler.c.obj                 │        521 │    8 │    8 │     0 │   63 │    63 │        0 │        450 │   450 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ipc_isr.c.obj                   │        518 │   44 │   32 │    12 │  409 │   409 │        0 │         35 │    35 │         30 │      30 │        0 │        0 │           0 │        0 │                  0 │
│ esp_clk_tree_common.c.obj           │        511 │    8 │    8 │     0 │    0 │     0 │        0 │        440 │   440 │         63 │      63 │        0 │        0 │           0 │        0 │                  0 │
│ cache_hal_esp32.c.obj               │        499 │   38 │    8 │    30 │  461 │   461 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ debug_helpers.c.obj                 │        498 │    0 │    0 │     0 │  498 │   498 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ memspi_host_driver.c.obj            │        488 │   95 │    0 │    95 │  393 │   393 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_hal.c.obj                 │        484 │    0 │    0 │     0 │    0 │     0 │        0 │        484 │   484 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-svfiprintf.o                 │        472 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │        472 │     472 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_os_func_app.c.obj         │        469 │   56 │    0 │    56 │  336 │   336 │        0 │         52 │    52 │         25 │      25 │        0 │        0 │           0 │        0 │                  0 │
│ rtc_module.c.obj                    │        459 │   28 │    4 │    24 │  188 │   188 │        0 │        243 │   243 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ freertos_hooks.c.obj                │        457 │  136 │  128 │     8 │   43 │    43 │        0 │        278 │   278 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ crosscore_int.c.obj                 │        440 │   16 │    8 │     8 │  248 │   248 │        0 │        130 │   130 │         46 │      46 │        0 │        0 │           0 │        0 │                  0 │
│ esp_clk_tree.c.obj                  │        432 │    0 │    0 │     0 │    0 │     0 │        0 │        403 │   403 │         29 │      29 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_gd.c.obj             │        430 │  127 │    0 │   127 │  303 │   303 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_flash_spi_init.c.obj            │        423 │   84 │    4 │    80 │    0 │     0 │        0 │        301 │   301 │         38 │      38 │        0 │        0 │           0 │        0 │                  0 │
│ newlib_init.c.obj                   │        402 │  144 │    0 │   144 │    0 │     0 │        0 │        258 │   258 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ app_startup.c.obj                   │        400 │    1 │    1 │     0 │    0 │     0 │        0 │        367 │   367 │         32 │      32 │        0 │        0 │           0 │        0 │                  0 │
│ xtensa_context.S.obj                │        394 │    0 │    0 │     0 │  394 │   394 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ flash_mmap.c.obj                    │        394 │    0 │    0 │     0 │  122 │   122 │        0 │        255 │   255 │         17 │      17 │        0 │        0 │           0 │        0 │                  0 │
│ esp_clk.c.obj                       │        372 │    9 │    0 │     9 │  339 │   339 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │       24 │                 24 │
│ libc_a-locale.o                     │        368 │    4 │    0 │     4 │    0 │     0 │        0 │          0 │     0 │        364 │     364 │        0 │        0 │           0 │        0 │                  0 │
│ esp_timer_impl_lac.c.obj            │        357 │    0 │    0 │     0 │  114 │   114 │        0 │        243 │   243 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ uart_hal_iram.c.obj                 │        356 │    0 │    0 │     0 │    0 │     0 │        0 │        316 │   316 │         40 │      40 │        0 │        0 │           0 │        0 │                  0 │
│ assert.c.obj                        │        352 │    0 │    0 │     0 │  352 │   352 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ uart_hal.c.obj                      │        351 │    0 │    0 │     0 │    0 │     0 │        0 │        351 │   351 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ brownout.c.obj                      │        350 │   51 │    4 │    47 │  215 │   215 │        0 │         79 │    79 │          5 │       5 │        0 │        0 │           0 │        0 │                  0 │
│ cpu.c.obj                           │        350 │    0 │    0 │     0 │  284 │   284 │        0 │         36 │    36 │         30 │      30 │        0 │        0 │           0 │        0 │                  0 │
│ startup.c.obj                       │        348 │   11 │   11 │     0 │   42 │    42 │        0 │        287 │   287 │          8 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ sleep_modes.c.obj                   │        344 │  120 │    0 │   120 │    0 │     0 │        0 │        162 │   162 │         26 │      26 │        0 │       36 │          36 │        0 │                  0 │
│ int_wdt.c.obj                       │        335 │    9 │    9 │     0 │  104 │   104 │        0 │        222 │   222 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ task_wdt_impl_timergroup.c.obj      │        335 │   12 │   12 │     0 │   31 │    31 │        0 │        292 │   292 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-findfp.o                     │        324 │  324 │  312 │    12 │    0 │     0 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ windowspill_asm.o                   │        311 │    0 │    0 │     0 │  311 │   311 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_efuse_startup.c.obj             │        302 │    0 │    0 │     0 │    0 │     0 │        0 │        246 │   246 │         56 │      56 │        0 │        0 │           0 │        0 │                  0 │
│ startup_funcs.c.obj                 │        280 │    0 │    0 │     0 │    0 │     0 │        0 │        208 │   208 │         72 │      72 │        0 │        0 │           0 │        0 │                  0 │
│ list.c.obj                          │        279 │    0 │    0 │     0 │  279 │   279 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-refill.o                     │        277 │    0 │    0 │     0 │    0 │     0 │        0 │        277 │   277 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_encrypt_hal_iram.c.obj    │        276 │   36 │    0 │    36 │  240 │   240 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ interrupts.c.obj                    │        276 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │        276 │     276 │        0 │        0 │           0 │        0 │                  0 │
│ sleep_gpio.c.obj                    │        255 │    0 │    0 │     0 │    0 │     0 │        0 │        227 │   227 │         28 │      28 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-makebuf.o                    │        246 │    0 │    0 │     0 │    0 │     0 │        0 │        246 │   246 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-impure.o                     │        244 │  244 │    0 │   244 │    0 │     0 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_time_impl.c.obj                 │        242 │   12 │   12 │     0 │  122 │   122 │        0 │        108 │   108 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_issi.c.obj           │        240 │  129 │    0 │   129 │  111 │   111 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ flash_ops.c.obj                     │        238 │   12 │    4 │     8 │   33 │    33 │        0 │        171 │   171 │         22 │      22 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_mxic.c.obj           │        238 │  129 │    0 │   129 │  109 │   109 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_chip_drivers.c.obj        │        234 │   28 │    0 │    28 │    0 │     0 │        0 │        206 │   206 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-fopen.o                      │        231 │    0 │    0 │     0 │    0 │     0 │        0 │        231 │   231 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-reent.o                      │        220 │    0 │    0 │     0 │    0 │     0 │        0 │        220 │   220 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ brownout_hal.c.obj                  │        196 │    0 │    0 │     0 │    0 │     0 │        0 │        196 │   196 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ regi2c_ctrl.c.obj                   │        188 │    8 │    0 │     8 │  180 │   180 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ heap_idf.c.obj                      │        185 │    0 │    0 │     0 │  185 │   185 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ota_ops.c.obj                   │        183 │    4 │    4 │     0 │    0 │     0 │        0 │        149 │   149 │         30 │      30 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-wsetup.o                     │        168 │    0 │    0 │     0 │    0 │     0 │        0 │        168 │   168 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ efuse_hal.c.obj                     │        164 │    0 │    0 │     0 │  164 │   164 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ highint_hdl.S.obj                   │        161 │    0 │    0 │     0 │  161 │   161 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ chip_info.c.obj                     │        158 │    0 │    0 │     0 │    0 │     0 │        0 │        158 │   158 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ abort.c.obj                         │        156 │    0 │    0 │     0 │  156 │   156 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ cache_err_int.c.obj                 │        146 │    0 │    0 │     0 │    0 │     0 │        0 │        146 │   146 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ partition_target.c.obj              │        146 │    0 │    0 │     0 │    0 │     0 │        0 │        146 │   146 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ xtensa_intr.c.obj                   │        143 │    0 │    0 │     0 │   26 │    26 │        0 │        117 │   117 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ system_time.c.obj                   │        141 │    8 │    8 │     0 │   31 │    31 │        0 │        102 │   102 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_memory_utils.c.obj              │        139 │    0 │    0 │     0 │  139 │   139 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_err.c.obj                       │        137 │    0 │    0 │     0 │  137 │   137 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_system_chip.c.obj               │        132 │    0 │    0 │     0 │  107 │   107 │        0 │         25 │    25 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ heap.c.obj                          │        131 │    0 │    0 │     0 │  131 │   131 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ log_lock.c.obj                      │        130 │    4 │    4 │     0 │  126 │   126 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_flash_os_func_noos.c.obj        │        130 │   40 │    0 │    40 │   90 │    90 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-flags.o                      │        129 │    0 │    0 │     0 │    0 │     0 │        0 │        129 │   129 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ lab6_1_basic_build.c.obj            │        126 │    0 │    0 │     0 │    0 │     0 │        0 │        126 │   126 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ipc_isr_handler.S.obj           │        123 │   16 │    0 │    16 │  107 │   107 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ heap_align_hw.c.obj                 │        118 │    0 │    0 │     0 │  118 │   118 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ port_common.c.obj                   │        110 │    0 │    0 │     0 │   80 │    80 │        0 │          0 │     0 │         30 │      30 │        0 │        0 │           0 │        0 │                  0 │
│ log_timestamp.c.obj                 │        108 │    4 │    4 │     0 │  104 │   104 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ stdatomic.c.obj                     │        107 │    8 │    0 │     8 │   99 │    99 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_system.c.obj                    │        106 │   20 │   20 │     0 │    0 │     0 │        0 │         86 │    86 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_cache_msync.c.obj               │        102 │   24 │    0 │    24 │   78 │    78 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libm_a-s_frexp.o                    │         99 │    0 │    0 │     0 │    0 │     0 │        0 │         99 │    99 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_rom_uart.c.obj                  │         96 │    0 │    0 │     0 │   96 │    96 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ tag_log_level.c.obj                 │         86 │    0 │    0 │     0 │   17 │    17 │        0 │         69 │    69 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ flash_brownout_hook.c.obj           │         76 │    2 │    2 │     0 │   74 │    74 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ mpu_hal.c.obj                       │         76 │    0 │    0 │     0 │    0 │     0 │        0 │         76 │    76 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ipc_isr_port.c.obj              │         74 │    0 │    0 │     0 │   40 │    40 │        0 │         34 │    34 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ ext_mem_layout.c.obj                │         72 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │         72 │      72 │        0 │        0 │           0 │        0 │                  0 │
│ cpu_region_protect.c.obj            │         71 │    0 │    0 │     0 │    0 │     0 │        0 │         51 │    51 │         20 │      20 │        0 │        0 │           0 │        0 │                  0 │
│ log.c.obj                           │         68 │    0 │    0 │     0 │   68 │    68 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ init.c.obj                          │         68 │    0 │    0 │     0 │    0 │     0 │        0 │         44 │    12 │         24 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ cache_esp32.c.obj                   │         67 │    8 │    0 │     8 │   59 │    59 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ panic_handler_asm.S.obj             │         64 │    0 │    0 │     0 │   64 │    64 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ state_asm--restore_extra_nw.o       │         62 │    0 │    0 │     0 │   62 │    62 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ state_asm--save_extra_nw.o          │         62 │    0 │    0 │     0 │   62 │    62 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-fwalk.o                      │         57 │    0 │    0 │     0 │    0 │     0 │        0 │         57 │    57 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ log_linked_list.c.obj               │         55 │    4 │    4 │     0 │    0 │     0 │        0 │         51 │    51 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ port_systick.c.obj                  │         50 │    0 │    0 │     0 │   50 │    50 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-printf.o                     │         50 │    0 │    0 │     0 │    0 │     0 │        0 │         50 │    50 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ reent_init.c.obj                    │         45 │    0 │    0 │     0 │    0 │     0 │        0 │         45 │    45 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ gpio_periph.c.obj                   │         40 │   40 │    0 │    40 │    0 │     0 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_timer_init.c.obj                │         38 │    0 │    0 │     0 │    0 │     0 │        0 │         30 │    30 │          8 │       8 │        0 │        0 │           0 │        0 │                  0 │
│ dport_access.c.obj                  │         37 │    0 │    0 │     0 │   37 │    37 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ xtensa_init.c.obj                   │         36 │    4 │    4 │     0 │   32 │    32 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_gpio_reserve.c.obj              │         36 │    8 │    0 │     8 │    0 │     0 │        0 │         28 │    28 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-vprintf.o                    │         36 │    0 │    0 │     0 │    0 │     0 │        0 │         36 │    36 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-sprint_r.o                   │         34 │    0 │    0 │     0 │    0 │     0 │        0 │         34 │    34 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ sar_periph_ctrl.c.obj               │         32 │    0 │    0 │     0 │    0 │     0 │        0 │         32 │    32 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-mbtowc_r.o                   │         32 │    0 │    0 │     0 │    0 │     0 │        0 │         32 │    32 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ interrupts--intlevel.o              │         32 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │         32 │      32 │        0 │        0 │           0 │        0 │                  0 │
│ bootloader_efuse.c.obj              │         30 │    0 │    0 │     0 │   30 │    30 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_cache_utils.c.obj               │         30 │    0 │    0 │     0 │   30 │    30 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ log_level.c.obj                     │         29 │    4 │    0 │     4 │    0 │     0 │        0 │         25 │    25 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ debug_helpers_asm.S.obj             │         29 │    0 │    0 │     0 │   29 │    29 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ syscalls.c.obj                      │         25 │    0 │    0 │     0 │    0 │     0 │        0 │         25 │    25 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-sysfcntl.o                   │         25 │    0 │    0 │     0 │    0 │     0 │        0 │         25 │    25 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-sysgettod.o                  │         24 │    0 │    0 │     0 │    0 │     0 │        0 │         24 │    24 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ reent_syscalls.c.obj                │         22 │    0 │    0 │     0 │    0 │     0 │        0 │         22 │    22 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-fseek.o                      │         21 │    0 │    0 │     0 │    0 │     0 │        0 │         21 │    21 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_rom_sys.c.obj                   │         19 │    0 │    0 │     0 │   19 │    19 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-localeconv.o                 │         19 │    0 │    0 │     0 │    0 │     0 │        0 │         19 │    19 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ util.c.obj                          │         18 │    4 │    4 │     0 │   14 │    14 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ libc_a-errno.o                      │         13 │    0 │    0 │     0 │    0 │     0 │        0 │         13 │    13 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_ipc_isr_routines.S.obj          │         10 │    0 │    0 │     0 │   10 │    10 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ flash_encrypt.c.obj                 │         10 │    0 │    0 │     0 │   10 │    10 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_efuse_api.c.obj                 │         10 │    0 │    0 │     0 │    0 │     0 │        0 │         10 │    10 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ pthread.c.obj                       │         10 │    0 │    0 │     0 │    0 │     0 │        0 │         10 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ int_asm--set_intclear.o             │          8 │    0 │    0 │     0 │    8 │     8 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ bootloader_mem.c.obj                │          8 │    0 │    0 │     0 │    0 │     0 │        0 │          8 │     8 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ esp_efuse_utility.c.obj             │          7 │    0 │    0 │     0 │    0 │     0 │        0 │          7 │     7 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ ubsan.c.obj                         │          5 │    0 │    0 │     0 │    5 │     5 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ clk_utils.c.obj                     │          5 │    0 │    0 │     0 │    5 │     5 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ getentropy.c.obj                    │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ pthread_cond_var.c.obj              │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ pthread_local_storage.c.obj         │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ pthread_rwlock.c.obj                │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ pthread_semaphore.c.obj             │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ cxx_guards.cpp.obj                  │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ cxx_init.cpp.obj                    │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ nvs_sec_provider.c.obj              │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ phy_override.c.obj                  │          5 │    0 │    0 │     0 │    0 │     0 │        0 │          5 │     5 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ log_write.c.obj                     │          4 │    4 │    0 │     4 │    0 │     0 │        0 │          0 │     0 │          0 │       0 │        0 │        0 │           0 │        0 │                  0 │
│ spi_bus_lock.c.obj                  │          4 │    0 │    0 │     0 │    0 │     0 │        0 │          0 │     0 │          4 │       4 │        0 │        0 │           0 │        0 │                  0 │
└─────────────────────────────────────┴────────────┴──────┴──────┴───────┴──────┴───────┴──────────┴────────────┴───────┴────────────┴─────────┴──────────┴──────────┴─────────────┴──────────┴────────────────────┘
```
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/f085388a-d641-4e3b-944d-b5228464120b" />

```c
Adding SPI flash device
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x12 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6372
load:0x40078000,len:15928
load:0x40080400,len:3880
entry 0x40080638
I (1426) boot: ESP-IDF v6.0-dev-1002-gbfe5caf58f 2nd stage bootloader
I (1428) boot: compile time Aug  6 2025 08:58:00
I (1429) boot: Multicore bootloader
I (2391) boot: chip revision: v3.0
I (2396) boot.esp32: SPI Speed      : 40MHz
I (2397) boot.esp32: SPI Mode       : DIO
I (2398) boot.esp32: SPI Flash Size : 2MB
I (2519) boot: Enabling RNG early entropy source...
I (2644) boot: Partition Table:
I (2644) boot: ## Label            Usage          Type ST Offset   Length
I (2645) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (2647) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (2648) boot:  2 factory          factory app      00 00 00010000 00100000
I (2764) boot: End of partition table
I (3700) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=09534h ( 38196) map
I (4164) esp_image: segment 1: paddr=0001955c vaddr=3ff80000 size=00024h (    36) load
I (4618) esp_image: segment 2: paddr=00019588 vaddr=3ffb0000 size=025e0h (  9696) load
I (5094) esp_image: segment 3: paddr=0001bb70 vaddr=40080000 size=044a8h ( 17576) load
I (5545) esp_image: segment 4: paddr=00020020 vaddr=400d0020 size=0efb8h ( 61368) map
I (6002) esp_image: segment 5: paddr=0002efe0 vaddr=400844a8 size=08b10h ( 35600) load
I (7579) boot: Loaded app from partition at offset 0x10000
I (7580) boot: Disabling RNG early entropy source...
I (7749) cpu_start: Multicore app
I (14862) cpu_start: Pro cpu start user code
I (14865) cpu_start: cpu freq: 160000000 Hz
I (14867) app_init: Application information:
I (14867) app_init: Project name:     lab6_1_basic_build
I (14869) app_init: App version:      1
I (14869) app_init: Compile time:     Aug  9 2025 13:50:34
I (14870) app_init: ELF file SHA256:  0200db97f...
I (14870) app_init: ESP-IDF:          v6.0-dev-1002-gbfe5caf58f
I (14871) efuse_init: Min chip rev:     v0.0
I (14871) efuse_init: Max chip rev:     v3.99
I (14872) efuse_init: Chip rev:         v3.0
I (14874) heap_init: Initializing. RAM available for dynamic allocation:
I (14876) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (14879) heap_init: At 3FFB2EA8 len 0002D158 (180 KiB): DRAM
I (14880) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (14881) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (14882) heap_init: At 4008CFB8 len 00013048 (76 KiB): IRAM
I (14998) spi_flash: detected chip: winbond
I (15011) spi_flash: flash io: dio
I (15031) main_task: Started on CPU0
I (15041) main_task: Calling app_main()
I (15041) LAB1: === Build Information ===
I (15041) LAB1: Project Name: lab6_1_basic_build
I (15041) LAB1: ESP-IDF Version: v6.0-dev-1002-gbfe5caf58f
I (15041) LAB1: Compile Date: Aug  9 2025
I (15051) LAB1: Compile Time: 14:00:00
I (15051) LAB1: Chip Model: esp32
I (15051) LAB1: Free Heap: 304636 bytes
I (15051) LAB1: Running... Counter: 0
I (16051) LAB1: Running... Counter: 1
I (17051) LAB1: Running... Counter: 2
I (18051) LAB1: Running... Counter: 3
I (19051) LAB1: Running... Counter: 4
I (20051) LAB1: Running... Counter: 5
I (21051) LAB1: Running... Counter: 6
I (22051) LAB1: Running... Counter: 7
I (23051) LAB1: Running... Counter: 8
I (24051) LAB1: Running... Counter: 9
I (24051) LAB1: Current free heap: 304636 bytes
I (25051) LAB1: Running... Counter: 10
I (26051) LAB1: Running... Counter: 11
I (27051) LAB1: Running... Counter: 12
I (28051) LAB1: Running... Counter: 13
I (29051) LAB1: Running... Counter: 14
I (30051) LAB1: Running... Counter: 15
I (31051) LAB1: Running... Counter: 16
I (32051) LAB1: Running... Counter: 17
I (33051) LAB1: Running... Counter: 18
I (34051) LAB1: Running... Counter: 19
I (34051) LAB1: Current free heap: 304636 bytes
I (35051) LAB1: Running... Counter: 20
I (36051) LAB1: Running... Counter: 21
I (37051) LAB1: Running... Counter: 22
I (38051) LAB1: Running... Counter: 23
I (39051) LAB1: Running... Counter: 24
I (40051) LAB1: Running... Counter: 25
I (41051) LAB1: Running... Counter: 26
I (42051) LAB1: Running... Counter: 27
I (43051) LAB1: Running... Counter: 28
I (44051) LAB1: Running... Counter: 29
I (44051) LAB1: Current free heap: 304636 bytes
I (45051) LAB1: Running... Counter: 30
I (46051) LAB1: Running... Counter: 31
I (47051) LAB1: Running... Counter: 32
I (48051) LAB1: Running... Counter: 33
I (49051) LAB1: Running... Counter: 34
I (50051) LAB1: Running... Counter: 35
I (51051) LAB1: Running... Counter: 36
I (52051) LAB1: Running... Counter: 37
I (53051) LAB1: Running... Counter: 38
I (54051) LAB1: Running... Counter: 39
I (54051) LAB1: Current free heap: 304636 bytes
I (55051) LAB1: Running... Counter: 40
I (56051) LAB1: Running... Counter: 41
I (57051) LAB1: Running... Counter: 42
I (58051) LAB1: Running... Counter: 43
I (59051) LAB1: Running... Counter: 44
I (60051) LAB1: Running... Counter: 45
I (61051) LAB1: Running... Counter: 46
I (62051) LAB1: Running... Counter: 47
I (63051) LAB1: Running... Counter: 48
I (64051) LAB1: Running... Counter: 49
I (64051) LAB1: Current free heap: 304636 bytes
I (65051) LAB1: Running... Counter: 50
I (66051) LAB1: Running... Counter: 51
I (67051) LAB1: Running... Counter: 52
```

```C
1) Docker vs Native
Docker ลงง่าย ไม่ปวดหัวเรื่องเวอร์ชัน เครื่องใครก็ build เหมือนกัน
Native ต้องลงเอง เสี่ยงเวอร์ชันชน แต่ build ไวกว่า

2) Build ใน Docker
cmake อ่าน CMakeLists → สร้าง build/ → คอมไพล์เป็น .elf → แปลงเป็น .bin → flash ได้

3) CMake Files
Root: ตั้งโปรเจกต์รวม
main/: ไฟล์หลักโปรแกรม
component/: ของเสริมแต่ละส่วน

4) .gitignore
กันไฟล์ build, .bin, sdkconfig ไม่ให้ติด git

5) Container Persistence
ไม่ mount → ไฟล์ build หาย
Mount → ไฟล์โค้ดอยู่, tools ใน image อยู่

6) Workflow
Docker: สะดวก, เหมือนกันทุกเครื่อง
Native: เร็วกว่า แต่เซ็ตยากกว่า
``` 



