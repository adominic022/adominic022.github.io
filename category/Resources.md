---
layout: category
title: Resources
---


<br />

# Machine Learning:

### Getting started:

- A great paper by Alex Graves:
    - [https://www.cs.toronto.edu/~graves/preprint.pdf](https://www.cs.toronto.edu/~graves/preprint.pdf)
- Andrew Ng's Standford intro course:
    - [https://www.coursera.org/learn/machine-learning](https://www.coursera.org/learn/machine-learning)

- Peter Domingo's Article:
    - [https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf)
- Colah's Blog:
    - [https://colah.github.io/](https://colah.github.io/)

### Tools:
- Tensorflow: [https://www.tensorflow.org/](https://www.tensorflow.org/)
- Pytorch: [https://pytorch.org/](https://pytorch.org/)

### Architectures:

- Convoluted Neural Networks:
    - [Introduction to CNNs](https://cs.nju.edu.cn/wujx/paper/CNN.pdf) 
    - [AlexNet](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)
    - [GoogleNet](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Szegedy_Going_Deeper_With_2015_CVPR_paper.pdf)
    - [ResNet](https://arxiv.org/pdf/1512.03385v1.pdf)

- Generative Adversarial Networks:
    - [GAN](https://arxiv.org/pdf/1406.2661v1.pdf)
    - [Generating Image Descriptions](https://arxiv.org/pdf/1412.2306v2.pdf)
    
- Natural Language Processing:
    - [Seq2Seq](https://arxiv.org/pdf/1409.3215.pdf)
    - [Attention](https://arxiv.org/pdf/1706.03762.pdf)
    - [LSTM](https://arxiv.org/pdf/1909.09586.pdf)
    - [Bert/Transformer](https://arxiv.org/pdf/1810.04805.pdf)


# Linux 
<br />

## [ManjaroOS](https://manjaro.org/)
- Install Pamac if not installed
- [Pacman](https://wiki.manjaro.org/index.php/Pacman_Overview)
    - Example of installing Slack:
```
sudo pacman -Syu && sudo pacman -S git base-devel
git clone https://aur.archlinux.org/slack-desktop.git
cd slack-desktop/
makepkg -sri
```

- [Snap](https://snapcraft.io/) or [installing on Arch](https://snapcraft.io/docs/installing-snap-on-arch-linux)

```
git clone https://aur.archlinux.org/snapd.git
cd snapd
makepkg -si
//Enable snap communication socket
sudo systemctl enable --now snapd.socket

//Snap Test:
$ sudo snap install hello-world
hello-world 6.3 from Canonical✓ installed
$ hello-world
Hello World!
```
- Disable Grub Delay
```
sudo nano /etc/default/grub
//Change GRUB_TIMEOUT value
sudo update-grub
```

- Check Swappiness
```
cat /proc/sys/vm/swappiness
```
    - To modify/Reduce:
    ```
    sudo nano /etc/sysctl.d/100-manjaro.conf
    ```
- Enable Trim for SSD (Need to Restart)
```
sudo systemctl enable fstrim.timer
```

- Check System Failures:
```
sudo systemctl --failed
```

- Other Ideas:
    - Nautilus & other Archive Managers
    - Sublime Text & VSCode
    - Liferea
    - Fragments (BitTorrent Client)
    - Gnome Boxes vs VirtualBox
    - Stacer
    

