list(APPEND LDFLAGS -lm)
set(RUN_OPTIONS output_large.enc /dev/null d 1234567890abcdeffedcba09876543211234567890abcdeffedcba0987654321)
set(HASH_PROGRAM_OUTPUT 1)
llvm_multisource(security-rijndael)
llvm_test_data(security-rijndael output_large.enc)
