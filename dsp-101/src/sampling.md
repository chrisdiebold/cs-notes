# Sampling, Aliasing, and Quantization

The starting point to understand is sampling and its affect on the signal of interest. To take an analog signal and convert it to a digital signal, we need to sample the signal using a device called an analog to digital converter (ADC). The ADC will measure the signal at rapid intervals, and these measurements are called samples. It will output a digital signal proportional to the amplitude of the analog signal at that instant.

This can be compared to looking at an object with only a strobe light for illumination. You can see the object only when the strobe light flashes. If the object is not moving, then everything looks pretty much the same as if we used a normal, continuous light source. Where things get interesting is when we look at a moving object with the strobe light. If the object is moving rapidly, then the appearance of the motion can be quite different that when viewed under normal light. We can also see strange effects even if the object is moving fairly slowly, and we reduce the rate of the strobe light enough.

We need a way to quantify how fast we must sample to accurately represent a given signal. We also need to better understand exactly what is happening when aliasing occurs. It may seem strange, but there are some instances when aliasing can be useful.

# Nyquist Sampling Rule 
To summarize, whenever you have a sampled signal, you cannot really be sure of its frequency. But if you assume that the rule was followed—that the signal was sampled at more than twice the frequency of the signal, then the sampled signal will really represent the same frequency as the actual signal prior to sampling. The critical frequency which the signal must not ever exceed, which is one half of the sampling frequency, is called the Nyquist frequency.

Normally, what is done is that the ADC converter frequency is selected to be high enough to sample the signal in which we want to perform digital signal processing on. To make sure that unwanted signals above the Nyquist frequency do not enter the ADC and cause aliasing, the desired signal in usually passed through an analog low pass filter, which attenuates any unwanted high frequency content signals, just prior to the ADC.

## Example: A Telephone
A common example is the telephone system. Our voices are assumed to have a maximum frequency of about 3600 Hz. At the microphone, our voice is filtered by an analog filter to eliminate, or at least substantially reduce, any frequencies above 3600 Hz. Then the microphone signal is sampled at 8000 Hz or 8 kHz. All subsequent digital signal processing occurs on this 8 kSPS (kilo-samples per second) signal. That is why if you hear music in the background while on the telephone, the music will sound flat or distorted. Our ears can detect up to about 15 kHz frequencies, and music generally has frequency content exceeding 3600 Hz. But little of this higher frequency content will be passed through the telephone system.

# Quantization
This fluctuating error signal will be seen as a form of noise or unwanted signal by the DSP. It is called quantization noise.

What is happening is that the quantization noise is always present and is, on average, the same level (any noiselike signal will rise and fall randomly, so we usually concern ourselves with the average level). But as the input signal decreases in level, the quantization noise becomes more significant in a relative sense. Eventually, for very small input signal levels, the quantization noise can become so significant that it degrades the quality of whatever signal processing is to be performed. Think of it as like static on a car radio. As you get further from the radio station, the radio signal gets weaker, and eventually the static noise makes it difficult or unpleasant to listen to, even if you increase the volume.

So what can we do if our signal sometimes is strong (0.503 for example), and other times is weak (0.00503 for example)? Another way of saying this is that the signal has a large dynamic range. The dynamic range describes the ratio between the largest and smallest value of the signal, in this case 100.

Suppose we exchange our 8 bit ADC for a 16 bit ADC? Then our maximum range is still from −1 to +1,


# Signal to Noise Ratio

SNR describes the power of the largest signal compared to the background noise. 

This can be very easily seen on a frequency domain or spectral plot of a signal. There can be many sources of noise, but for now, we are only considering the quantization noise introduced by the ADC sampling.

SNR is usually expressed in decibels (denoted dB), using a logarithmic scale. The SNR of an ideal ADC can be determined by the following equation:

```latex
snr_quantization (dB) = 6.02 * (Number of bits) + 1.76
```

Basically, for each additional bit of the ADC, 6 dB of SNR is gained. An 8 bit ADC is capable of representing a signal with an SNR of about 48 dB, a 12 bit ADC can do better at 72 dB, and a 16 bit will give up to 96 dB. This only accounts for the effect of quantization noise; in practice there are other effects that also will degrade SNR in a system.

A decibel is simply a signal power ratio, similar to percentage. But because of the extremely high ratios commonly used (a billion is not uncommon), it is convenient to express this logarithmically. The logarithmic expression also allow chains of circuits or signal processing operations each with its own ratio (say of output power to input power) to simply be added up to find the final ratio.

Where people commonly get confused is in differentiating between signal levels or amplitude (voltage if an analog circuit) and signal power. Power measurements are virtual in the digital world, but can be directly measured in analog circuits in which DSP systems interface with.

There are 2 definitions of dB commonly used:

```
dB_voltage = dB_digital value = 20 * log(voltage signal 1 / voltage signal 2)
```

```
dB_power = 10* log(power signal 1 / power signal 2)
```

So dB can refer to many different ratios. But it is easy to get confused whether to use to multiplicative factor of 10 or 20, without understanding the reasoning behind this.

Voltage squared is proportional to power. If a given voltage is doubled in a circuit, it requires four times as much power. This goes back to a basic Ohm's law equation.

```
Power = Voltage ^2 / Resistance
```

In the digital world, the concept of resistance and power do not exist. A given signal has specific amplitude, expressed in a digital numerical system (such as signed fractional or integer for example).
Understanding dB increases using the two measurement methods is important. Let us look at doubling of the amplitude ratio and doubling of the power ratio.


