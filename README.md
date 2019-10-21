# podman-installer-mac <!-- omit in toc -->

"Turn-key" installer for Podman on MacOS. Tennessee Tech University Senior Capstone project.

**Status:** Not started yet

1. [Primary epic](#primary-epic)

## Primary epic

**Story:**
As a user of MacOS, I would like the ability to use Podman on my system as a “turn-key” solution, so that I don’t have to wade through the extensive documentation posted [here](https://github.com/containers/libpod/blob/master/docs/tutorials/mac_client.md).

**Background:**

Currently, Podman is very difficult to set up on MacOS, because the `podman` client on MacOS is actually only a remote client, that requires a connection to a Linux host to work. I want the ability to follow a very simple set of instructions, and have Podman up and running on my Macbook in under 10 minutes, utilizing a Linux virtual machine.

**Acceptance Criteria:**

1. A Linux virtual machine is automatically installed, configured, and started when I run the “turn-key” solution.
1. The virtual machine has everything it needs to act as the remote host for the MacOS podman client
1. The MacOS podman client is automatically installed if it isn’t present already on the system
1. After running the “turn-key” solution, I can then immediately run `podman run hello-world:latest` and it will show the same output as `docker run hello-world:latest` without having to do any extra configuration
1. Only Free Open Source Software is used in the final solution
1. All source code, documentation, and supporting materials are hosted in GitHub, and are licensed as Free and Open Source (License TBD).
1. The solution is tested and supported on MacOS Mojave.

**Technical Notes:**

1. Automated Configuration Management
    1. Ansible?
    1. Puppet?
    1. Chef?
    1. Other?
1. VM Runner
   1. Vagrant?
   1. VMWare?
   1. VirtualBox?
   1. [Zhyve](https://medium.com/@fiercelysw/virtualization-on-mac-os-x-using-vagrant-part-1-be0f0e291938)?
   1. Something else?
1. A solution utilizing Ansible would be great since Red Hat are the creators of both Podman and Ansible.
1. The operating system of the virtual machine should, barring any unforeseen technical barriers, be CentOS 8. CentOS because it is the open source version of Red Hat Enterprise Linux and is well supported in the Red Hat ecosystem, and version 8 because it is the latest version, which the Red Hat team is using for their Podman development. This is not listed as an acceptance criteria due to the technical nature, but it should be seen as a requirement unless significant technical barriers start preventing it from happening.
1. An invite should be extended to the Podman stakeholders at Red Hat to weigh in on this story, and to let them know that this work is happening.
