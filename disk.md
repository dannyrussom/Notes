# Disk Management


**see list of disks**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">lsblk -f</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>

**create a mount location**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo mkdir -p /media/danny/wdssd</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>

**mount disk**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo mount -t ntfs /dev/sda1 /media/ps/mypassport</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>



<br>

<br>

**unmount disk**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo umount /media/danny/wdssd</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>

**clear mount problems**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo umount /dev/sda1
sudo ntfsfix /dev/sda1</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>


## Notes

- you can setup automatic mouting with <button onclick="navigator.clipboard.writeText(this.innerText)">sudo chown danny:danny /media/danny/MyPassport</button>, then <button onclick="navigator.clipboard.writeText(this.innerText)">sudo nano /etc/fstab</button>, then <button onclick="navigator.clipboard.writeText(this.innerText)">UUID=3A2C1F2A2C1EF123  /media/danny/MyPassport  ntfs  defaults,nofail,x-systemd.automount  0  0</button> (replace the UUID, check <button onclick="navigator.clipboard.writeText(this.innerText)">lsblk -f</button>)

