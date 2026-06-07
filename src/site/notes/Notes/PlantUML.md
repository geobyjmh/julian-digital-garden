---
{"dg-publish":true,"permalink":"/notes/plant-uml/","dg-note-properties":{}}
---

- Link: [[Notes/Diagrams-as-Code (DaC)\|Diagrams-as-Code (DaC)]]

**PlantUML** is an open-source, text-based tool used to rapidly create clean, professional Unified Modeling Language (UML) diagrams and other structured visualizations. Instead of manually dragging and dropping shapes in a graphical editor, users write simple, intuitive human-readable code to define components and their interactions (such as `User -> (Sign In)`). The software then automatically calculates the optimal layout, spacing, and styling to generate the diagram. It is heavily utilized by software engineers, system architects, and technical writers to document complex systems, map software design patterns, and maintain diagrams directly alongside source code in version control systems.

# Tools
- [Open-source tool that uses simple textual descriptions to draw beautiful UML diagrams.](https://plantuml.com/) 

# PlantUML Examples
## Example 1
```
@startuml

package "DepthAI Pipeline" {
    [Pipeline] as pipeline
    [MonoCamera] as mono
    [XLinkOut] as xout
    pipeline -> mono : createMonoCamera()
    mono -> xout : link(output)
}

@enduml
```
![Pasted image 20260607100106.png](/img/user/Images/Pasted%20image%2020260607100106.png)

## Example 2
```
@startuml

start

:Create dai.Device(pipeline) as device;
:queue_mono = device.getOutputQueue(name="left_camera", maxSize=4, blocking=False);

while (loop forever)
    :in_mono = queue_mono.get();
    if (in_mono is not None) then (yes)
        :frame = in_mono.getCvFrame();
        :cv2.imshow("preview", frame);
    endif
    if (cv2.waitKey(1) == ord('q')) then (yes)
        :print('Key "q" pressed');
        :cv2.destroyAllWindows();
        stop
    endif
endwhile

-[hidden]->

@enduml
```
![Pasted image 20260607100355.png](/img/user/Images/Pasted%20image%2020260607100355.png)

# Reference

PlantUML (2026) _PlantUML: Open-source tool that uses simple textual description to draw beautiful UML diagrams_. Available at: [https://plantuml.com/](https://plantuml.com/) (Accessed: 7 June 2026).

Wikipedia (2026) _PlantUML_. Available at: [https://en.wikipedia.org/wiki/PlantUML](https://en.wikipedia.org/wiki/PlantUML) (Accessed: 7 June 2026).

Last Updated: 07/06/26
