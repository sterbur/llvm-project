add_header_library(
  threads_utils
  HDRS
    thread_utils.h
)

add_entrypoint_object(
  thrd_create
  SRCS
    thrd_create.cpp
  HDRS
    ../thrd_create.h
  DEPENDS
    errno_h
    linux_syscall_h
    mmap
    support_common_h
    sys_syscall_h
    threads_h
    threads_utils
    __errno_location
)

add_entrypoint_object(
  thrd_join
  SRCS
    thrd_join.cpp
  HDRS
    ../thrd_join.h
  DEPENDS
    linux_syscall_h
    munmap
    support_common_h
    sys_syscall_h
    threads_h
    threads_utils
)
