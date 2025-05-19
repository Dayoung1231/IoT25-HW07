# IoT25-HW07
- - -

## Distance Estimation Model
<pre><code>
distance(m) = 10 ^ (((-59)-RSSI)/(10*2.0))

// RSSI = Received signal strength (dBm)
// -59 = RSSI value measured at a distance of 1 meter (dBm)
// 2.0 = Path loss exponent
</code></pre>

- - -

