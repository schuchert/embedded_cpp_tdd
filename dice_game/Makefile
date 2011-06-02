ifneq (,$(wildcard *.sbd))
include $(wildcard *.sbd)
endif
SDETOP = /cygdrive/c/sde-6.06/sde
CUT_DIR = ../cpputest

TEST_SRCS = \
	$(CUT_DIR)/src/CppUTest/CommandLineArguments.cpp \
	$(CUT_DIR)/src/CppUTest/CommandLineTestRunner.cpp \
	$(CUT_DIR)/src/CppUTest/JUnitTestOutput.cpp \
	$(CUT_DIR)/src/CppUTest/MemoryLeakAllocator.cpp \
	$(CUT_DIR)/src/CppUTest/MemoryLeakDetector.cpp \
	$(CUT_DIR)/src/CppUTest/MemoryLeakWarningPlugin.cpp \
	$(CUT_DIR)/src/CppUTest/SimpleString.cpp \
	$(CUT_DIR)/src/CppUTest/TestFailure.cpp \
	$(CUT_DIR)/src/CppUTest/TestHarness_c.cpp \
	$(CUT_DIR)/src/CppUTest/TestOutput.cpp \
	$(CUT_DIR)/src/CppUTest/TestPlugin.cpp \
	$(CUT_DIR)/src/CppUTest/TestRegistry.cpp \
	$(CUT_DIR)/src/CppUTest/TestResult.cpp \
	$(CUT_DIR)/src/CppUTest/Utest.cpp \
	$(CUT_DIR)/src/CppUTest/UtestPlatform.cpp 

PROG = dice_game

SRCS = $(TEST_SRCS) \
	$(wildcard *.cpp)

LOADLIBES = -lstdc++ 
CXXFLAGS += -O1 -g
CXXFLAGS += -ffunction-sections -I$(CUT_DIR)/include
LDFLAGS += -Wl,--gc-sections

FLOAT = yes

include $(SDETOP)/examples/make.mk
