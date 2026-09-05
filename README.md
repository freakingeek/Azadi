<div align="center">

<img src="https://raw.githubusercontent.com/freakingeek/Azadi/main/image.png" alt="Azadi" width="512">

# Azadi · آزادی

**A focused DNS filter for a quieter, cleaner, and more private Persian web.**

![Rules](https://img.shields.io/badge/rules-63-3b82f6?style=flat-square)
![Format](https://img.shields.io/badge/format-AdGuard%20DNS-67b279?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-8b5cf6?style=flat-square)

</div>

Azadi blocks domains associated with advertising, tracking, intrusive website elements, and censorship-related services. Its AdGuard-style rules work with AdGuard Home, AdGuard DNS, AdGuard applications, and compatible content blockers.[^1]

## Get the subscription URL

Open [`Azadi.txt`](./Azadi.txt), select **Raw**, and copy the resulting URL. A valid subscription URL points directly to the plain-text file and usually looks like this:

```text
https://raw.githubusercontent.com/freakingeek/Azadi/main/hosts.txt
```

## AdGuard Home

AdGuard Home is the recommended way to apply Azadi to every device on a network.

1. Open the AdGuard Home administration dashboard.
2. Make sure **Protection** is enabled and your devices use AdGuard Home as their DNS server.
3. Go to **Filters → DNS blocklists**.
4. Select **Add blocklist → Add a custom list**.
5. Enter `Azadi` as the name and paste the raw subscription URL.
6. Select **Save** or **Add**, then make sure the new list is enabled.
7. Use **Check for updates** to download the latest rules immediately.

To verify the setup, open **Query Log** and visit a Persian website that normally loads advertising or tracking requests. Matching requests should appear as blocked by Azadi.

Azadi uses AdGuard’s recommended Adblock-style DNS syntax. A rule such as `||example.com^` blocks `example.com` and its subdomains. See the [AdGuard Home blocklist documentation](https://github.com/AdguardTeam/AdGuardHome/wiki/Hosts-Blocklists) for syntax details.

## AdGuard applications

Menu names vary slightly between platforms, but the process is the same:

1. Open **Settings → Filters** or **Ad blocking → Filters**.
2. Open **Custom filters** and select **Add custom filter**.
3. Paste the raw subscription URL, continue through the confirmation screen, and enable Azadi.

AdGuard for Android also accepts a local file path. The browser extension accepts either a URL or a local file. Refer to AdGuard’s documentation for [Android filters](https://adguard.com/kb/adguard-for-android/features/settings/#filters) and [browser-extension custom filters](https://adguard.com/kb/adguard-browser-extension/features/filters/#custom-filters).

## AdGuard DNS

For AdGuard Private DNS:

1. Open the AdGuard DNS dashboard.
2. Go to **Servers**, then select your server.
3. Open **Blocklists → Custom → Add custom blocklist**.
4. Enter `Azadi`, paste the raw subscription URL, and select **Add**.

See AdGuard’s [custom blocklist guide](https://adguard-dns.io/kb/private-dns/setting-up-filtering/blocklists/#custom-blocklists) for more information.

## Troubleshooting

- Confirm that the subscription URL opens as plain text and begins with the Azadi header.
- Refresh the list manually after changing the URL or updating the file.
- Clear the device or browser DNS cache if an old DNS answer remains cached.
- Check AdGuard Home’s **Query Log** to identify a blocked domain if a website stops working.
- Allowlist only the affected domain instead of disabling the entire list.
- DNS filtering blocks network requests but cannot remove every empty space or first-party advertisement embedded directly in a page.

## License

Azadi is distributed under the [MIT License](./LICENSE).

---

[^1]: Azadi rests on work carried forward by generous souls who gave their time and care to a freer web. With heartfelt gratitude to [PersianBlocker](https://github.com/MasterKia/PersianBlocker), its late creator Sayyed Ali “Master” Kia, its team, and every contributor. May their work and memory endure.
