nixos-configs
---

# (WIP) Description

At the moment, this is used with virtualbox/qemu to build a NixOS system from scratch.

# Instructions
Download installation iso from [NixOS Downloads](https://nixos.org/download). For example:

`https://channels.nixos.org/nixos-23.11/latest-nixos-minimal-x86_64-linux.iso`

## Virtualbox 
  
Configure a new VM in Virtualbox. Boot the Virtualbox VM with latest nixos minimal iso.

At the command prompt, follow the [NixOS Manual](https://nixos.org/manual/nixos/stable/#sec-installation)

Once the `configuration.nix` file has been generated with the `nixos-generate-config --root /mnt` command, edit the file with the following changes:

```nix
  nix.settings.experimental-features = [ "nix-command" "flakes" ];
```



