################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
LSS += \
attiny48_stepper_driver.lss \

FLASH_IMAGE += \
attiny48_stepper_driver.hex \

SIZEDUMMY += \
sizedummy \


# All Target
all: attiny48_stepper_driver.elf secondary-outputs

# Tool invocations
attiny48_stepper_driver.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: AVR C Linker'
	avr-gcc -Wl,-Map,attiny48_stepper_driver.map -mmcu=attiny48 -o"attiny48_stepper_driver.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

attiny48_stepper_driver.lss: attiny48_stepper_driver.elf
	@echo 'Invoking: AVR Create Extended Listing'
	-avr-objdump -h -S attiny48_stepper_driver.elf  >"attiny48_stepper_driver.lss"
	@echo 'Finished building: $@'
	@echo ' '

attiny48_stepper_driver.hex: attiny48_stepper_driver.elf
	@echo 'Create Flash image (ihex format)'
	-avr-objcopy -R .eeprom -O ihex attiny48_stepper_driver.elf  "attiny48_stepper_driver.hex"
	@echo 'Finished building: $@'
	@echo ' '

sizedummy: attiny48_stepper_driver.elf
	@echo 'Invoking: Print Size'
	-avr-size --format=berkeley -t attiny48_stepper_driver.elf
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(ASM_DEPS)$(FLASH_IMAGE)$(ELFS)$(LSS)$(S_DEPS)$(SIZEDUMMY)$(S_UPPER_DEPS) attiny48_stepper_driver.elf
	-@echo ' '

secondary-outputs: $(LSS) $(FLASH_IMAGE) $(SIZEDUMMY)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
