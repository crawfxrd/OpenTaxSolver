# SPDX-License-Identifier: GPL-2.0-or-later

CC = gcc
CFLAGS += -O -Wall
BUILD = bin

GTK2_FLAGS = -Wno-deprecated-declarations `pkg-config --cflags gtk+-2.0`
GTK2_LIBS = `pkg-config --libs gtk+-2.0`

.PHONY: all
all: $(BUILD)/taxsolve_US_1040_2017 \
	$(BUILD)/taxsolve_US_1040_Sched_C_2017 \
	$(BUILD)/taxsolve_PA_40_2017 \
	$(BUILD)/taxsolve_NJ_1040_2017 \
	$(BUILD)/taxsolve_VA_760_2017 \
	$(BUILD)/taxsolve_NC_D400_2017 \
	$(BUILD)/taxsolve_OH_IT1040_2017 \
	$(BUILD)/taxsolve_NY_IT201_2017 \
	$(BUILD)/taxsolve_MA_1_2017 \
	$(BUILD)/taxsolve_CA_540_2017 \
	$(BUILD)/convert_results2xfdf \
	$(BUILD)/ots_gui2 \
	$(BUILD)/universal_pdf_file_modifier

.PHONY: run
run: $(BUILD)/ots_gui2
	./$<

$(BUILD)/ots_gui2: src/gtk/ots_gui2.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) $(GTK2_FLAGS) -o $@ $^ $(GTK2_LIBS)

$(BUILD)/taxsolve_US_1040_2017: src/taxsolve_US_1040_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_US_1040_Sched_C_2017: src/taxsolve_US_1040_Sched_C_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_CA_540_2017: src/taxsolve_CA_540_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_NC_D400_2017: src/taxsolve_NC_D400_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_PA_40_2017: src/taxsolve_PA_40_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_NJ_1040_2017: src/taxsolve_NJ_1040_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_OH_IT1040_2017: src/taxsolve_OH_IT1040_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_VA_760_2017: src/taxsolve_VA_760_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_NY_IT201_2017: src/taxsolve_NY_IT201_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/taxsolve_MA_1_2017: src/taxsolve_MA_1_2017.c #src/taxsolve_routines.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/universal_pdf_file_modifier: src/universal_pdf_file_modifier.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

$(BUILD)/convert_results2xfdf: src/convert_results2xfdf.c
	@mkdir -p $(BUILD)
	$(CC) $(CFLAGS) -o $@ $^

.PHONY: clean
clean:
	$(RM) -rv $(BUILD)
