# Wind River Workbench generated Makefile.
# Do not edit!!!
#
# The file ".wrmakefile" is the template used by the Wind River Workbench to
# generate the makefiles of this project. Add user-specific build targets and
# make rules only(!) in this project's ".wrmakefile" file. These will then be
# automatically dumped into the makefiles.

WIND_HOME := $(subst \,/,$(WIND_HOME))
WIND_BASE := $(subst \,/,$(WIND_BASE))
WIND_USR := $(subst \,/,$(WIND_USR))

all : pre_build main_all post_build

_clean ::
	@echo "make: removing targets and objects of `pwd`"

TRACE=0
TRACEON=$(TRACE:0=@)
TRACE_FLAG=$(TRACEON:1=)

MAKEFILE := Makefile

FLEXIBLE_BUILD := 1

BUILD_SPEC = PPC603gnu
DEBUG_MODE = 1
ifeq ($(DEBUG_MODE),1)
MODE_DIR := Debug
else
MODE_DIR := NonDebug
endif
OBJ_DIR := .
WS_ROOT_DIR := C:/Users/mhsrobotics/Desktop/Robot\ 2013
PRJ_ROOT_DIR := $(WS_ROOT_DIR)/2012RobotCode



#Global Build Macros
PROJECT_TYPE = DKM
DEFINES = 
EXPAND_DBG = 0


#BuildSpec specific Build Macros
VX_CPU_FAMILY = ppc
CPU = PPC603
TOOL_FAMILY = gnu
TOOL = gnu
TOOL_PATH = 
CC_ARCH_SPEC = -mcpu=603 -mstrict-align -mno-implicit-fp  -mlongcall
LIBPATH = 
LIBS = 

IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/WPILib -I$(WIND_BASE)/target/h/wrn/coreip -I. 

IDE_LIBRARIES = $(WIND_BASE)/target/lib/WPILib.a 

IDE_DEFINES = 



#BuildTool flags
ifeq ($(DEBUG_MODE),1)
DEBUGFLAGS_C-Compiler = -g
DEBUGFLAGS_C++-Compiler = -g
DEBUGFLAGS_Linker = -g
DEBUGFLAGS_Partial-Image-Linker = 
DEBUGFLAGS_Librarian = 
DEBUGFLAGS_Assembler = -g
else
DEBUGFLAGS_C-Compiler = -O2 -fstrength-reduce -fno-builtin
DEBUGFLAGS_C++-Compiler = -O2 -fstrength-reduce -fno-builtin
DEBUGFLAGS_Linker = -O2 -fstrength-reduce -fno-builtin
DEBUGFLAGS_Partial-Image-Linker = 
DEBUGFLAGS_Librarian = 
DEBUGFLAGS_Assembler = -O2 -fstrength-reduce -fno-builtin
endif


#Project Targets
PROJECT_TARGETS = ButtonTest/$(MODE_DIR)/ButtonTest.out


#Rules

# ButtonTest
ifeq ($(DEBUG_MODE),1)
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -g
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -g
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -g
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -g
else
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_C-Compiler = -O2 -fstrength-reduce -fno-builtin
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_C++-Compiler = -O2 -fstrength-reduce -fno-builtin
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Linker = -O2 -fstrength-reduce -fno-builtin
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Partial-Image-Linker = 
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Librarian = 
ButtonTest/$(MODE_DIR)/% : DEBUGFLAGS_Assembler = -O2 -fstrength-reduce -fno-builtin
endif
ButtonTest/$(MODE_DIR)/% : IDE_INCLUDES = -I$(WIND_BASE)/target/h -I$(WIND_BASE)/target/h/WPILib -I$(WIND_BASE)/target/h/wrn/coreip -I. 
ButtonTest/$(MODE_DIR)/% : IDE_LIBRARIES = $(WIND_BASE)/target/lib/WPILib.a 
ButtonTest/$(MODE_DIR)/% : IDE_DEFINES = 
ButtonTest/$(MODE_DIR)/% : PROJECT_TYPE = DKM
ButtonTest/$(MODE_DIR)/% : DEFINES = 
ButtonTest/$(MODE_DIR)/% : EXPAND_DBG = 0
ButtonTest/$(MODE_DIR)/% : VX_CPU_FAMILY = ppc
ButtonTest/$(MODE_DIR)/% : CPU = PPC603
ButtonTest/$(MODE_DIR)/% : TOOL_FAMILY = gnu
ButtonTest/$(MODE_DIR)/% : TOOL = gnu
ButtonTest/$(MODE_DIR)/% : TOOL_PATH = 
ButtonTest/$(MODE_DIR)/% : CC_ARCH_SPEC = -mcpu=603 -mstrict-align -mno-implicit-fp  -mlongcall
ButtonTest/$(MODE_DIR)/% : LIBPATH = 
ButtonTest/$(MODE_DIR)/% : LIBS = 
ButtonTest/$(MODE_DIR)/% : OBJ_DIR := ButtonTest/$(MODE_DIR)

OBJECTS_ButtonTest =

ButtonTest/$(MODE_DIR)/ButtonTest.out : $(OBJECTS_ButtonTest)
	$(TRACE_FLAG)if [ ! -d "`dirname "$@"`" ]; then mkdir -p "`dirname "$@"`"; fi;echo "building $@";rm -f "$@";nmppc $(OBJECTS_ButtonTest) $(IDE_LIBRARIES) | tclsh $(WIND_BASE)/host/resource/hutils/tcl/munch.tcl -c ppc > $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccppc $(DEBUGFLAGS_Linker) $(CC_ARCH_SPEC) -fdollars-in-identifiers -Wall $(ADDED_CFLAGS) $(IDE_INCLUDES) $(ADDED_INCLUDES) -DCPU=$(CPU) -DTOOL_FAMILY=$(TOOL_FAMILY) -DTOOL=$(TOOL) -D_WRS_KERNEL   $(DEFINES)  -o $(OBJ_DIR)/ctdt.o -c $(OBJ_DIR)/ctdt.c; $(TOOL_PATH)ccppc -r -nostdlib -Wl,-X -T $(WIND_BASE)/target/h/tool/gnu/ldscripts/link.OUT -o "$@" $(OBJ_DIR)/ctdt.o $(OBJECTS_ButtonTest) $(IDE_LIBRARIES) $(LIBPATH) $(LIBS)  $(ADDED_LIBPATH) $(ADDED_LIBS) && if [ "$(EXPAND_DBG)" = "1" ]; then plink "$@";fi

ButtonTest/$(MODE_DIR)/ButtonTest_compile_file : $(FILE) ;

_clean :: ButtonTest/$(MODE_DIR)/ButtonTest_clean

ButtonTest/$(MODE_DIR)/ButtonTest_clean : 
	$(TRACE_FLAG)if [ -d "ButtonTest" ]; then cd "ButtonTest"; rm -rf $(MODE_DIR); fi

force : 



-include $(PRJ_ROOT_DIR)/*.makefile

-include *.makefile

main_all : external_build $(PROJECT_TARGETS)
	@echo "make: built targets of `pwd`"

# entry point for extending the build
external_build ::
	@echo ""

# main entry point for pre processing prior to the build
pre_build :: $(PRE_BUILD_STEP) generate_sources
	@echo ""

# entry point for generating sources prior to the build
generate_sources ::
	@echo ""

# main entry point for post processing after the build
post_build :: $(POST_BUILD_STEP) deploy_output
	@echo ""

# entry point for deploying output after the build
deploy_output ::
	@echo ""

clean :: external_clean $(CLEAN_STEP) _clean

# entry point for extending the build clean
external_clean ::
	@echo ""
