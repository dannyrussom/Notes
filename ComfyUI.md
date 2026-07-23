# comfyUI
## REMOTELY (Ubutnu and Windows)

**ON SERVER**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">CUDA_VISIBLE_DEVICES=0 python3 main.py --listen 0.0.0.0 --port 8188</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Ubuntu Server</button>
</div>

<br>

<br>

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">python main.py --listen 0.0.0.0 --port 8188</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Win Server</button>
</div>

<br>

<br>

**ON CLIENT**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">ssh -L 8188:172.20.172.87:8188 dr@172.20.172.87</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Ubuntu Server</button>
</div>

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">root</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">pass</button>
</div>

<br>

<br>


<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">ssh -L 8188:172.20.172.133:8188 PS@172.20.172.133</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Win server</button>
</div>


<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">19970620</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Pass</button>
</div>

<br>

<br>



_________________________________________________

## LOCALLY (Ubuntu)


<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">source venv/bin/activate</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Activate venv</button>
</div>

<br>

<br>


<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">python3 main.py</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Run main.py</button>
</div>

<br>

<br>