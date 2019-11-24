# passthrough_helper_ubuntu


Source of vfio-pci-override-vga.sh is http://vfio.blogspot.com/2015/05/

Find the GRUB_CMDLINE_LINUX line and within the quotes add either "intel_iommu=on" or "amd_iommu=on", depending on whether your platform is Intel or AMD. And then add "rd.driver.pre=vfio-pci".
