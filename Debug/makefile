################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := MiniProjekat5-Luka-Markovic-97-2018
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
MiniProjekat5-Luka-Markovic-97-2018.elf \

MAP_FILES += \
MiniProjekat5-Luka-Markovic-97-2018.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
MiniProjekat5-Luka-Markovic-97-2018.list \

OBJCOPY_HEX += \
MiniProjekat5-Luka-Markovic-97-2018.hex \


# All Target
all: main-build

# Main-build Target
main-build: MiniProjekat5-Luka-Markovic-97-2018.elf secondary-outputs

# Tool invocations
MiniProjekat5-Luka-Markovic-97-2018.elf MiniProjekat5-Luka-Markovic-97-2018.map: $(OBJS) $(USER_OBJS) C:\Users\LmArK\Desktop\CubeProjects\MiniProjekat5-Luka-Markovic-97-2018\STM32F103C6TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "MiniProjekat5-Luka-Markovic-97-2018.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\LmArK\Desktop\CubeProjects\MiniProjekat5-Luka-Markovic-97-2018\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="MiniProjekat5-Luka-Markovic-97-2018.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

MiniProjekat5-Luka-Markovic-97-2018.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "MiniProjekat5-Luka-Markovic-97-2018.list"
	@echo 'Finished building: $@'
	@echo ' '

MiniProjekat5-Luka-Markovic-97-2018.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "MiniProjekat5-Luka-Markovic-97-2018.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) MiniProjekat5-Luka-Markovic-97-2018.elf MiniProjekat5-Luka-Markovic-97-2018.hex MiniProjekat5-Luka-Markovic-97-2018.list MiniProjekat5-Luka-Markovic-97-2018.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
