---
description: Before we can develop Java, we should prepare for Java Environment, right?
---

# Setup

### Installing Java Development Kit (JDK)

JDK is software package that includes tools and components for develop and running Java applications. These are general steps to install JDK :

1. **Download JDK**, please visit and choose JDK version that you want in this link [https://www.oracle.com/id/java/technologies/downloads/](https://www.oracle.com/id/java/technologies/downloads/)
2. **Installing JDK**, open JDK file that you download before, and follow steps that provided.
3. **Verify Installation**, open terminal or prompt or CMD, then type `java -version` to verify installed java version on your machine.&#x20;

If after execute `java -version` you can see installed java version like this :

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Congrats ! Java installed successfully in your machine !

But if you cannot see installed Java version, it means you should setup `environment variables` on your machine. Maybe these following steps can help your issue :

1. If your machine using **Windows** as operating systems, you can click Windows button, then type `Environment Variable`, then choose this&#x20;

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

2. Then click `Environment Variables` button&#x20;

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

3. On `System Variables` section, click on `Path`, then click `Edit` button
4. Then add your Java's bin path (you can click `New` button). e.g -> `C:\Program Files\Java\jdk-11.0.16\bin`
5. Then save your changes, and try yo verify Java version.
6. Good luck !

### Installing Integrated Development Environment (IDE)

Actually you can use **Code Editor** instead of **IDE**. But IMO, using Java IDE can make your development proses faster and easier. These are IDE that you can use for develop Java source code

1.  **IntelliJ IDEA**

    In my opinion, so far IntelliJ IDEA is the most powerful Java IDEA. You can visit this link for choose IntelliJ version that you want -> [https://www.jetbrains.com/idea/download](https://www.jetbrains.com/idea/download). You can use community version for free, or ultimate version for paid software.
2.  **NetBeans**

    NetBeans is one of the best open source IDE for develop Java. You can visit this link -> [https://netbeans.apache.org/download/index.html](https://netbeans.apache.org/download/index.html)
3.  **Eclipse**

    Actually I have no enough experience to give review for this IDE, but you can visit this link to try Eclipse -> [https://eclipseide.org/](https://eclipseide.org/)
