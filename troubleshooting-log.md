# Troubleshooting Log

## Issue: Ubuntu Server VM lost internet access

**Date:** 2026-05-07  
**System:** ubuntu01  
**Severity:** Medium  

### Symptoms

- Could not ping google.com
- Could ping local router
- `apt update` failed
- SSH still worked from local network

### Troubleshooting Steps

1. Checked IP address using `ip a`
2. Checked default gateway using `ip route`
3. Tested DNS using `nslookup google.com`
4. Tested external IP connectivity using `ping 8.8.8.8`
5. Checked Proxmox virtual bridge settings
6. Restarted networking service

### Root Cause

DNS was not configured correctly after changing the VM network settings.

### Resolution

Updated DNS server configuration and confirmed name resolution worked.

### Verification

- `ping google.com` worked
- `apt update` completed successfully
- VM could reach external websites

### Lesson Learned

Always test IP connectivity and DNS separately when diagnosing network issues.
