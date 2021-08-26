---
title: "A Brief Guide on Setting Up Java with WSL and VSCode"
date: 2021-08-25
categories: en

classes:
  - wide
---

Recently I had the chance to set up the whole dev environment on a 2018 Surface Pro. So far I really love it! Smaller size, touch screen, and keyboard (oh, so much better than any Apple keyboard)! Though with only 128GB SSD and 8GB RAM, I have to be extra cautious about what software to install to save some space and resources, so I have to stick with a smaller IDE instead of Intellij which is simply superior in terms of Java development. And since Windows has WSL which is pretty mature right now, I decide to set up my Java dev environment with WSL and VSCode.

And this is a *brief* guide on how to do it. Some details can be found in the links I listed.

## WSL

First things first, you need to have WSL, or WSL2, installed and configured. Microsoft has great documentation on how to do it. Simply follow the steps in this [link](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

You may need to restart your PC once or twice.

I chose Ubuntu 20 LTS as my Linux distribution (always up to date) and [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) as my default terminal instead of the old cmd prompt. Windows Terminal is such a beautiful and modern tool to use in 2021, definitely better than Mac's default Terminal.

## VSCode

Next, VSCode, just google it and download the latest version for Windows.

After VSCode is installed, you should install the **Remote - WSL** first so that VSCode knows it when you launch VSCode from WSL.

Then, open a project or simply open VSCode from WSL by issue `code your-project` from WSL. After that, install the **Extension Pack for Java** extension and make sure it's installed for WSL implied by its green color.

You will see a new tab named **Configure Java Runtime** opened which will be configured in the next step.

## Java

Now it's time to install Java, or JDK specifically. There are multiple distributions and versions of JDK maintained by different organizations available to public, and as a personal flavor, I chose Amazon Correto 11 (targetting OpenJDK 11). You can follow this [link](https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/generic-linux-install.html) to install it on your WSL with Ubuntu distro.

You can verify your installation with `java -version` and `javac -version`. If you see version 11 returned from both commands, you are ready to configure it in VSCode.

Now, switch back to VSCode, reload the window, and choose Amazon corretto 11 as your Java runtime under **Configure Java Runtime** tab. You should be able to select it from the dropdown menu. The jvm path should be similar to `/usr/lib/jvm/java-11-amazon-corretto`.

## Hello World

Finally, it's time to run some code.

Run a simple *Hello World* or any legit Java code to test.

```Java
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

If you see `Hello World` printed out in the terminal like the following, you've successfully set up the Java dev env with WSL and VSCode. Congrats!

```bash
>>> /usr/bin/env /usr/lib/jvm/java-11-amazon-corretto/bin/java -Dfile.encoding=UTF-8 -cp /home/me/.vscode-server/data/User/workspaceStorage/eb4d70c17ac883444bf6265d01bc83fe/redhat.java/jdt_ws/hello-world_11bb32c8/bin HelloWorld 
Hello World!
```
