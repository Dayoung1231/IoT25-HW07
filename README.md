# IoT25-HW07


## Distance Estimation Model
<pre><code>
distance(m) = 10 ^ (((-59)-RSSI)/(10*2.0))

// RSSI = Received signal strength (dBm)
// -59 = RSSI value measured at a distance of 1 meter (dBm)
// 2.0 = Path loss exponent
</code></pre>

- - -

## Test and Analyze
- Graph of Distance estimation model & RSSI value measured at actual distance
  
![output (1).png](attachment:00ac2e37-bcc5-4737-8383-e9779d120c79:output_(1).png)


### Why is there a slight difference with the model
1. **Environmental Factors**
* Multipath Propagation
* Signal Absorption
* Signal Interference
2. **Model Simplification**
* Although the model set pathLossExponent to a fixed value (2.0), it can vary in the range of 1.6 to 3.5 in real-world environments.
3. **Volatility of BLE signal (BLE Signal Fluctuation)**
* The BLE signal fluctuates over time.
* Therefore, it is more accurate to use the average value after multiple measurements, rather than a single sample.
