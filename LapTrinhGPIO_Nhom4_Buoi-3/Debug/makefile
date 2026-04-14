################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (14.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE-20260323T122231Z-3-001/SDK_1.0.3_NUCLEO-F401RE/shared/Utilities/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE-20260323T122231Z-3-001/SDK_1.0.3_NUCLEO-F401RE/shared/Drivers/STM32F401RE_StdPeriph_Driver/src/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE-20260323T122231Z-3-001/SDK_1.0.3_NUCLEO-F401RE/shared/Drivers/CMSIS/Source/subdir.mk
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


BUILD_ARTIFACT_NAME := LapTrinhGPIO_Nhom4_Buoi-3
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
LapTrinhGPIO_Nhom4_Buoi-3.elf \

MAP_FILES += \
LapTrinhGPIO_Nhom4_Buoi-3.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
LapTrinhGPIO_Nhom4_Buoi-3.list \

OBJCOPY_HEX += \
LapTrinhGPIO_Nhom4_Buoi-3.hex \


# All Target
all: main-build

# Main-build Target
main-build: LapTrinhGPIO_Nhom4_Buoi-3.elf secondary-outputs

# Tool invocations
LapTrinhGPIO_Nhom4_Buoi-3.elf LapTrinhGPIO_Nhom4_Buoi-3.map: $(OBJS) $(USER_OBJS) D:\Buoi3NHom4\LapTrinhGPIO_Nhom4_Buoi-3\STM32F401RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "LapTrinhGPIO_Nhom4_Buoi-3.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Buoi3NHom4\LapTrinhGPIO_Nhom4_Buoi-3\STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="LapTrinhGPIO_Nhom4_Buoi-3.map" -Wl,--gc-sections -static -L"C:\Users\ADMIN\Downloads\SDK_1.0.3_NUCLEO-F401RE-20260323T122231Z-3-001\SDK_1.0.3_NUCLEO-F401RE\lib_stm" --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

LapTrinhGPIO_Nhom4_Buoi-3.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "LapTrinhGPIO_Nhom4_Buoi-3.list"
	@echo 'Finished building: $@'
	@echo ' '

LapTrinhGPIO_Nhom4_Buoi-3.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "LapTrinhGPIO_Nhom4_Buoi-3.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) LapTrinhGPIO_Nhom4_Buoi-3.elf LapTrinhGPIO_Nhom4_Buoi-3.hex LapTrinhGPIO_Nhom4_Buoi-3.list LapTrinhGPIO_Nhom4_Buoi-3.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
