# Clash

## Shortcuts

- Reload daemon <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl daemon-reload</button> 
- Enable service <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl enable clash</button> 
- Start service <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl start clash</button>
- Restart service <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl restart clash</button>
- See status <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl status clash</button>
- See logs <button onclick="navigator.clipboard.writeText(this.innerText)">sudo journalctl -u clash -f</button>



**Start Clash**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo /usr/local/bin/clash -d /home/danny/.config/clash/</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>


**Kill all Clash Processes**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo killall clash</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>


**Restart Clash**

<div style="display:inline-flex;align-items:center;gap:8px;">
  <code id="cmd1" style="padding:6px 8px;border-radius:6px;background:black;">sudo killall clash && sudo /usr/local/bin/clash -d /etc/clash/ &</code>
  <button onclick="navigator.clipboard.writeText(this.previousElementSibling.innerText)">Copy</button>
</div>

<br>

<br>


## Notes

- When you start clash, you can specify the config file location with the '-d' flag.
- You can customize for each website using rules and proxy groups inside the config.yaml file.

## Automation with Services

- Create a systemd service file in <button onclick="navigator.clipboard.writeText(this.innerText)">cd /etc/systemd/system</button>, and put the above command in ExecStart.

- Reload daemon <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl daemon-reload</button>, enable the service <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl enable clash</button>, and start it <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl start clash</button>.

- Restart it <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl restart clash</button> if you made any changes.

- See the proxy logs in real time <button onclick="navigator.clipboard.writeText(this.innerText)">sudo journalctl -u clash -f</button>. '-u' flag is for unit/service, and '-f' flag is for following the logs in real-time.
_________________________________________________
