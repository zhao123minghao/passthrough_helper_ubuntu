# passthrough_helper_ubuntu


Source of vfio-pci-override-vga.sh is http://vfio.blogspot.com/2015/05/

Find the GRUB_CMDLINE_LINUX line and within the quotes add either "intel_iommu=on" or "amd_iommu=on", depending on whether your platform is Intel or AMD. And then add "rd.driver.pre=vfio-pci".

For virsh edit: within the \<features\> section, remove everything between the <hyperv> tags, including the tags themselves.  In their place add the following tags:

    <kvm>
      <hidden state='on'/>
    </kvm>

Additionally, within the <clock> tag, find the timer named hypervclock, remove the line containing this tag completely.  Save and exit the edit session.
