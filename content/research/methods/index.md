---
title: Instrumentation and Methods
weight: 1
subtitle: Improving single-sided NMR instrumentation and use
summary: |
    *Improving single-sided NMR instrumentation and use*
    
    We develop pulse sequences, nuclear hyperpolarization, and accessory hardware that improve the ease of use, accuracy, and quality of single-sided NMR measurements.
show_date: false
image:
    preview_only: true
    # Use Hugo's image processing
    # This will output a 400px-wide image (maintains aspect ratio)
    filename: featured.webp
---

One premise of single-sided NMR is that good measurements shouldn't require a million-dollar magnet. Our instrumentation work extends that premise: we build tools that are inexpensive, well documented, and easy enough for an undergraduate to run and maintain.

Single-sided magnets have a sensitive region that's wide but only a few hundred microns tall, so positioning a sample precisely within it is time-consuming and easy to get wrong by hand. In 2023, we built a tilt-tip sample stage that positions samples with high linear and angular precision, automatically optimizing that position to improve resolution several-fold ([*Magnetic Resonance in Chemistry*, 2023]({{< ref "/publications/2023-kiple-automated-spatial-resolution" >}})). Two years later, we designed and constructed *RAMM*, an open-source, 3D-printer-based robotic magnetic field mapper that competes with commercial products costing one-to-two orders of magnitude more ([*HardwareX*, 2025]({{< ref "/publications/2025-li-ramm-robotic-magnetic-field-mapper" >}})); we use it to characterize the field profiles of our own magnets and of arrays of smaller magnets that produce custom field shapes.

Looking ahead, we're also laying the groundwork for dynamic nuclear polarization (DNP) on a single-sided platform, and want to keep increasing access to NMR more broadly through open-source hardware, code, and pulse sequences — building on *RAMM* and the growing availability of open-source field-modeling software to develop low-cost NMR hardware customized to specific applications. These projects particularly suit students interested in engineering, open science, and the connection between NMR theory and the hardware that makes a measurement possible.