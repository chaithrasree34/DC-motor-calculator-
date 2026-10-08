# DC-motor-calculator-
# DC Motor Calculator

print("DC MOTOR CALCULATOR")
print("-------------------")

# Input values
V = float(input("Enter supply voltage (V): "))
Ia = float(input("Enter armature current (A): "))
Ra = float(input("Enter armature resistance (Ohm): "))
speed = float(input("Enter motor speed (RPM): "))
torque = float(input("Enter motor torque (N-m): "))

# Back EMF
Eb = V - (Ia * Ra)

# Input electrical power
Pin = V * Ia

# Mechanical output power
Pout = (2 * 3.14159 * speed * torque) / 60

# Efficiency
efficiency = (Pout / Pin) * 100

# Display results
print("\n--- DC Motor Results ---")
print(f"Back EMF          = {Eb:.2f} V")
print(f"Input Power       = {Pin:.2f} W")
print(f"Output Power      = {Pout:.2f} W")
print(f"Motor Efficiency  = {efficiency:.2f}%")

# Check motor condition
if Eb > 0:
    print("The DC motor is operating normally.")
else:
    print("Check the input values.")