# Introduction

The book that these notes  were based on grew out of a need for Altera (now Intel) marketing and technical sales people to have an intuitive-level understanding of digital signal processing (DSP) fundamentals and applications, to better work on issues that our customers face as they implement DSP systems. 

This book was intended for executive and midlevel management, marketing, technical sales and field engineers, business development, and others—who can benefit from a basic knowledge of the fundamental principles of DSP.

The goal is to provide a basic tutorial on DSP. Limited Mathematics. 

## What is DSP?
DSP is performing operations on a digital signal of some sort and using a digital semiconductor device. Most commonly, multipliers and adders are used. If you can multiply and add, you can probably understand DSP. Actually, signal processing was around long before digital electronics. Examples of this are radios and TVs. Early tuners used analog circuits with variable capacitors to dial a station. Resistors, capacitors, and vacuum tubes were used to either attenuate or amplify different frequencies or to provide frequency shifting. These are examples of basic signal-processing applications. The signals were analog signals, and the circuits doing the processing were analog, as was the final output.

Today, most signal processing is performed digitally. The reason is that digital circuits have progressively become cheaper and faster, as well as due to the inherent advantages of repeatability, tolerance, and consistency that digital circuits enjoy compared to analog circuits.

If the signal is not in a digital form, then it must be first converted, or digitized. A device called an analog-to-digital converter (ADC) is used. If the output signal needs to be analog, then it is converted back using a digital-to-analog converter (DAC). Of course, many signals are already digitized and can be processed by digital circuits directly.


