# Compile all shared objects for TMB models
all: fit_theta.so opt_theta.so fit_theta_beta.so opt_theta_beta.so opt_beta.so fit_theta_nn.so opt_theta_nn.so fit_theta_beta_nn.so opt_theta_beta_nn.so opt_beta_nn.so

# Compile fit_theta.cpp into fit_theta.so
fit_theta.so: fit_theta.cpp
	Rscript --vanilla -e "TMB::compile('fit_theta.cpp', '-O0 -g')"

# Compile opt_theta.cpp into opt_theta.so
opt_theta.so: opt_theta.cpp
	Rscript --vanilla -e "TMB::compile('opt_theta.cpp', '-O0 -g')"

# Compile fit_theta_beta.cpp into fit_theta_beta.so
fit_theta_beta.so: fit_theta_beta.cpp
	Rscript --vanilla -e "TMB::compile('fit_theta_beta.cpp', '-O0 -g')"

# Compile opt_theta_beta.cpp into opt_theta_beta.so
opt_theta_beta.so: opt_theta_beta.cpp
	Rscript --vanilla -e "TMB::compile('opt_theta_beta.cpp', '-O0 -g')"

# Compile opt_beta.cpp into opt_beta.so
opt_beta.so: opt_beta.cpp
	Rscript --vanilla -e "TMB::compile('opt_beta.cpp', '-O0 -g')"

# Compile fit_theta_nn.cpp into fit_theta_nn.so
fit_theta_nn.so: fit_theta_nn.cpp
	Rscript --vanilla -e "TMB::compile('fit_theta_nn.cpp', '-O0 -g')"

# Compile opt_theta_nn.cpp into opt_theta_nn.so
opt_theta_nn.so: opt_theta_nn.cpp
	Rscript --vanilla -e "TMB::compile('opt_theta_nn.cpp', '-O0 -g')"

# Compile fit_theta_beta_nn.cpp into fit_theta_beta_nn.so
fit_theta_beta_nn.so: fit_theta_beta_nn.cpp
	Rscript --vanilla -e "TMB::compile('fit_theta_beta_nn.cpp', '-O0 -g')"

# Compile opt_theta_beta_nn.cpp into opt_theta_beta_nn.so
opt_theta_beta_nn.so: opt_theta_beta_nn.cpp
	Rscript --vanilla -e "TMB::compile('opt_theta_beta_nn.cpp', '-O0 -g')"

# Compile opt_beta_nn.cpp into opt_beta_nn.so
opt_beta_nn.so: opt_beta_nn.cpp
	Rscript --vanilla -e "TMB::compile('opt_beta_nn.cpp', '-O0 -g')"


# Clean up generated files
clean:
	rm -f *.so *.o
