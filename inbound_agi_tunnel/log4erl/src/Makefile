# leave these lines alone
.SUFFIXES: .erl .beam .yrl

.erl.beam:
	erlc -o $(EBIN_DIR) -W $<

.yrl.erl:
	erlc -o $(EBIN_DIR) -W $<

SOURCE_DIR=src
EBIN_DIR=../../ebin
INCLUDE_DIR=include
#SRC=$(wildcard $(SOURCE_DIR)/*)
ERL = erl -o $(EBIN_DIR) -I ${INCLUDE_DIR}
SRC = src

# Here's a list of the erlang modules you want compiling
# If the modules don't fit onto one line add a \ character
# to the end of the line and continue on the next line
# Edit the lines below
MODS = log4erl_sup log4erl file_appender log_manager logger_guard log4erl_utils dummy_appender log_formatter

all:	compile

#compile: ${MODS:%=%.beam} #application
#compile: ${SRC}/${MODS:%=%.beam}

compile: ${MODS:%=%.beam}

clean:
	rm -rf ${EBIN_DIR}/*.beam erl_crash.dump
