# Detect OS and set correct shared library extension
UNAME := $(shell uname -s)

ifeq ($(UNAME), Darwin)  # macOS
  EXT = so
else ifeq ($(UNAME), Linux)
  EXT = so
else  # Assume Windows (MSYS or Cygwin)
  EXT = dll
endif

# Define all target shared object files
TMB_TARGETS = fit_theta.$(EXT) opt_theta.$(EXT) fit_theta_beta.$(EXT) opt_theta_beta.$(EXT) opt_beta.$(EXT) \
              fit_theta_nn.$(EXT) opt_theta_nn.$(EXT) fit_theta_beta_nn.$(EXT) opt_theta_beta_nn.$(EXT) opt_beta_nn.$(EXT)

# Default target: compile all shared objects
all: $(TMB_TARGETS)

# General rule to compile any .cpp file into a shared object
%.$(EXT): %.cpp
	Rscript --vanilla -e "TMB::compile('$<', '-O0 -g')"

# Clean up generated shared object and intermediate files
clean:
	rm -f $(TMB_TARGETS) *.o