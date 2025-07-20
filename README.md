# Distance-MEasurement-with-an-ultrasonic-sensor-HY-SRF05

## **HY-SRF05 Distance Sensor: Operation & Working Principle**

The **HY-SRF05** is an ultrasonic distance sensor used to measure distances by emitting sound waves and calculating the time it takes for the echo to return after hitting an object. It is widely used in robotics and automation for obstacle detection and distance measurement.

---

### **Pinout Description**

* **Vcc**: Connects to the 5V power supply.
* **GND**: Connects to the ground of the system.
* **Trig**: The trigger pin used to initiate the measurement by sending an ultrasonic pulse.
* **Echo**: Outputs the time duration of the received echo signal.
* **OUT**: An optional digital output that generates pulses based on the detection (not used in basic applications).

---

### **Working Principle**

1. A 10 microsecond HIGH signal is applied to the **Trig** pin.
2. This triggers the sensor to emit 8 ultrasonic bursts at 40 kHz.
3. The **Echo** pin then goes HIGH and stays HIGH until the emitted wave returns after hitting an object.
4. The time duration of the HIGH pulse on the Echo pin represents the total time taken for the sound to travel to the object and back.
5. Using the known speed of sound in air (approximately **0.0343 cm/µs**), the distance is calculated with the formula:

   $$
   \text{Distance} = \frac{\text{Time} \times 0.0343}{2}
   $$

   The division by 2 accounts for the round trip of the ultrasonic wave.

---

### **Key Features**

* **Measuring Range**: 2 cm to approximately 450 cm.
* **Accuracy**: High precision in distance measurement.
* **Fail-Safe Timeout**: If no object is detected, the Echo pin returns LOW after 38 milliseconds.

---

### **Modes of Connection**

1. **Two-Wire Mode**: Trig and Echo are connected to separate Arduino pins.
2. **One-Wire Mode**: Both Trig and Echo are connected to the same Arduino pin to simplify wiring.

---

### **Software Support**

* The sensor can be programmed using standard Arduino functions.
* **NewPing** Library: Simplifies code and offers additional features such as automatic timeout and cleaner syntax for pinging.

---

### **Application Areas**

* Obstacle avoidance in robotics.
* Distance monitoring systems.
* Water level detection.
* Smart parking systems.

