cmake_minimum_required(VERSION 2.8.12)
project(BIGNUM C)

add_definitions(-std=c99)

add_library(bignum
            src/bn/add.c
            src/bn/asm/x86_64-gcc.c
            src/bn/bn.c
            src/bn/bytes.c
            src/bn/cmp.c
            src/bn/convert.c
            src/bn/ctx.c
            src/bn/div.c
            src/bn/exponentiation.c
            src/bn/gcd.c
            src/bn/generic.c
            src/bn/jacobi.c
            src/bn/montgomery_inv.c
            src/bn/montgomery.c
            src/bn/mul.c
            src/bn/prime.c
            src/bn/random.c
#            src/bn/rsaz_exp.c
            src/bn/shift.c
            src/bn/sqrt.c
            src/cbb.c
            src/buf.c
            src/mem.c
            src/thread.c
            src/thread_none.c
            src/thread_pthread.c
            src/thread_win.c
            src/err.c)
target_include_directories(bignum PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
