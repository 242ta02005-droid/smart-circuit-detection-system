# smart-circuit-detection-system
# Automatic Generator Controller

LOW_VOLTAGE = 200
NORMAL_VOLTAGE = 230
MAX_TEMPERATURE = 80

print("==============================")
print("   AUTOMATIC GENERATOR CONTROLLER")
print("==============================")

voltage = float(input("Enter supply voltage (V): "))
temperature = float(input("Enter generator temperature (°C): "))

print("\nSupply Voltage:", voltage, "V")
print("Generator Temperature:", temperature, "°C")

if temperature > MAX_TEMPERATURE:
    print("\n🔴 GENERATOR OVERHEATING")
    print("⚠️ Generator stopped for protection")

elif voltage < LOW_VOLTAGE:
    print("\n⚠️ LOW SUPPLY VOLTAGE")
    print("🟢 Generator STARTED")
    print("⚡ Backup power supplied")

elif voltage >= NORMAL_VOLTAGE:
    print("\n🟢 MAIN SUPPLY NORMAL")
    print("🔴 Generator STOPPED")
    print("⚡ Load supplied by main power")

else:
    print("\n🟡 SUPPLY VOLTAGE LOW")
    print("🟢 Generator STARTED")
    print("⚡ Backup power supplied")

print("\nAutomatic generator control completed.")
