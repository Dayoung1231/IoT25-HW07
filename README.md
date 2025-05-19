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
  
![IoT25-HW07_graph](https://github.com/user-attachments/assets/748543fd-330c-4683-b602-1dc3aabd6f06)



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

- - -


## Demo video
https://drive.google.com/file/d/1HXvBzpx5t_Fgruiuz1zJ3qvO1O_kR6uc/view?usp=sharing


