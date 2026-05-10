# `west`-based Custom ZMK Configuration for MoErgo Go60

![MoErgo Logo](moergo_logo.png)

This template repository provides `west`-based ZMK configuration for the MoErgo Go60 wireless split contoured keyboard.
You can use this template repository to develop your own keymap and build your own ZMK firmware to run on your Go60 using ZMK/Zephyr's upstream `west` toolchain.

**NOTE: You can also customize the layout of your Go60 keyboard with the [Go60 Layout Editor](https://my.go60.com) web app, or the [official ZMK configuration repository template](https://github.com/moergo-keyboards/go60-zmk-config).
For most users, the Go60 Layout Editor is the recommended and simpler option. More information is available at the official MoErgo Go60 Support site (see resources below).**

These steps will get you using your keymap on your keyboard in the fastest time possible. It uses the GitHub Actions feature to build your firmware online.

If you are looking to dig deeper into ZMK and develop new functionality, it is recommended to follow the steps of installing ZMK as found on the official ZMK documentation site (linked below).

## Resources
- The [official MoErgo Go60 Support](https://moergo.com/go60-support) web site. Go60 documentation and other technical resources.
- The [official MoErgo Discord Server](https://moergo.com/discord). Instant conversations with other Go60 users.

- The [official ZMK Documentation](https://zmk.dev/docs) web site. Find the answers to many of your questions about ZMK Firmware.
- The [official ZMK Discord Server](https://discord.gg/8cfMkQksSB). Instant conversations with other ZMK developers and users. Great technical resource!

- The [official MoErgo ZMK Distribution](https://github.com/moergo-sc/zmk). Repository for ZMK firmware customized for Go60 and Glove80.

## Instructions
1. Log into, or sign up for, your personal GitHub account.
2. Create your own repository using this repository as a template ([instructions](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template])) and check it out on your local computer.
3. Add your chosen configuration such as keymap to the `config` directory as described in [the ZMK documentation](https://zmk.dev/docs/user-setup)
4. Commit and push your changes to your personal repo. Upon pushing it, GitHub Actions will start building a new version of your firmware with the updated keymap.

## Firmware Files
To locate your firmware files and reflash your Go60:
1. log into GitHub and navigate to your personal config repository you just uploaded your keymap changes to.
2. Click "Actions" in the main navigation, and in the left navigation click the "Build" link.
3. Select the desired workflow run in the centre area of the page (based on date and time of the build you wish to use). You can also start a new build from this page by clicking the "Run workflow" button.
4. After clicking the desired workflow run, you should be presented with a section at the bottom of the page called "Artifacts". This section contains the results of your build, in a file called `firmware.zip`.
5. Download `firmware.zip` and extract it to reveal two files, `go60_lh-zmk.uf2` and `go60_rh-zmk.uf2`: these are the firmware for the left and right sides of the keyboard respectively.
6. Flash the firmware to Go60 according to the user documentation on the official Go60 Support website (linked above). *Note that unlike firmware built with the standard Go60 toolchain, you must select the correct firmware file to upload to each half of the keyboard.*

Your keyboard is now ready to use.
