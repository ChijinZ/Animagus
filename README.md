# Animagus

Animagus is the prototype of imitation-based ransomware attack, which aims to help I/O based ransomware detection techniques realize the limits of their feature engineering.

The related paper (Limits of I/O Based Ransomware Detection: An Imitation Based Attack) was accepted by S&P'23.

Notice: this is just a research prototype. We only release the executable for ethic consideration.

We tested this executable in Win 11 environment.

## Usage

First, unzip the prototype and the patterns:

```shell
unzip animagus-prototype.zip
unzip imitated_patterns.zip
```

Next, rename one of the patterns to ``pattern``:

```shell
mv 7_27_firefox_log.txt.pattern pattern
```

Finally, execute the ``imitation.exe``. The $PATH is the directory containing files that you want to encrypt:

```shell
.\imitation.exe -p $PATH
```

After execution, all important files (e.g., txt, doc, ppt, sql) in the directory are encrypted. For ethic consideration, we did not release the prototype version that can encrypt all files in the victim system. We believe this released executable is enough for others to conduct relevant evaluation.