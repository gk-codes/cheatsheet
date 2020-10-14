# Nmap

Run a fullport scan \(`-p-` with service detection \(`-sV`\) and script scan \(`-sC`\), do not ping the host \(`-Pn`\). Store the output \(`-oA` in all formats \(nmap, gnmap, xml\):

```bash
sudo nmap -p- -Pn -sV -sC IPADDRESS -oA nmap_fullport_IPADDRESS
```

{% hint style="info" %}
It is important to run nmap with `sudo`
{% endhint %}

