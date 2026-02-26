![Lazy logo](logo.svg)

# Quick Share MD

A minimal Markdown editor focused on quick writing and frictionless sharing via URL.

# [Try now!](https://carlosmpv.github.io/quickshare-md/?q=H4sIAAAAAAAAA71Vy3LbRhC84yumSpeYkkhHlhKVKk6KNuWybNKyRLmkSipVWgAjYMPFLrS74EOnfES+MF+SnuVDzi2+hCcsMNPTO90z3KOrThczmtbKM01GWZYNqdFWN8rQRPlZ6RaWuNTReXpwRRe4JGfpMWUtvI7aVqRsSQ9eF1E7azgECoCTD3Ot6Mv1uA/YvT16xyp2nkOW9Wis50yt57nmBY4IOmRbuBLwJco0bCOFqCLj40de5U75ErDOx6KLAS/fGFfMDnMlhISflGuQb9a13rsFXUS6dX4WspsatVTFpAMVrmldusVDylO5YcoFLIDmuSrq9YlyrtWcA6mAixvjFuFMiN/WbLedOCAdEQdIiaP7nyIvIxqpfr5HiN/y6m/TctN5v0nzbEv2AY/CyUa5MEptew4uwhpvNYT5d0vkGoG9VkY/CZpcCW1NhESKbSO1jY4iUNBdKMZ+hXzR5QAhuLe0TFtACvBGsYWOtetAhXJVzMARRKapaKMsWphYoL5uWpMOqNMFybzlnN5Kcy3ehv6zDCDxJXCWfd+nyxZdEEZrR51lRPRbHWMbzgaDQnnjQtPO+xVIdHlfu0HymXDjw6b8/bv/HPoiO+oTePtIcdUmDV716bN0ie7PwdrfU1zogoXdWorEKznSdQF28aryqq372fEu8W30hvZpei9ZAe74WjF60Ib72UkfXWhXSYjEZqvApiM3XNRWFxivTy6uZ2GHsCYizYQEbZcaHZSFiZ52bR5dTj53Xj+sxFWwiE92sI5auEkH+AiXMmqFC/395187+Xs9HXq9dNyaSQA+OXHSnP2BQJQK44CJSgdVFK57VnKsGwyLTHjiLOZs1FI3XbOzr2FbxVroGAkG5XyVKm4DhcgmKHRti2F+jsk9Jow9qhH10twqj/rlGYXWYF62RZKpm85EDQOCZ5TRQ6/h5pkANdCmYjwACu6i86USq6JgLisgWe4bPDf45fH1++NwMdz+lncfF1dHw8mwevdyHG8Gk+n1j8MPF9Pbo1l7fX7cjV8tbbl/WZ3+Oq2YTx4n5tZ3J9X0h5fVqNGDN1dXd9HY5ej4po53i8WYr0an+3dT/3Qq6K+/weP/N7UXkH1oZD1U9caqkG+ny1dWPYDdYo03rXd/cBHXDo0E4iVbJMlyxLeyS38ZcDb3ehufjXQojNINeyxAWTSyWaNbPWNJvXIDwkvYXoubkzXXTmDlrYxK23lZ9XDwyKX6qCOrV4YX2weeYBvAGHOsLdCahCE8/gH27tt7FwcAAA==) 

## Features

* Live preview
* URL-encoded document state
* Keyboard shortcuts
* Block-based editing model


## How It Works
The page is composed of editable blocks.

Each block behaves as follows:

* When focused, it becomes a `<textarea>` for editing.
* When blurred, it renders its content as Markdown.

The entire document state is serialized, compressed, and encoded into the URL query string, enabling instant sharing without a backend.

State management is implemented using Web Components.


## How to Use

1. Open the editor:
   [https://carlosmpv.github.io/quickshare-md](https://carlosmpv.github.io/quickshare-md)
2. Start typing.
3. Press `Enter` twice to render the previous paragraph.
4. Press `Ctrl + S` to save as Markdown file.
5. Copy and share the URL.


## Technical Notes

* Markdown rendering output is sanitized using DOMPurify.
* There is no persistence layer — the URL **is** the document.
* No server, no database, no accounts.


## Limitations

* The maximum content length is limited by the maximum URL length supported by the browser.

  * Workaround: split content into multiple notes and link them together.
    Example subpage:
    [https://carlosmpv.github.io/quickshare-md/?q=H4sIAAAAAAAAAxXKwQ2AMAgF0LtT/MSR7AJISW2kpRE4uL3xnd+Og8ZSgee5qMlWru5gS60gDmi/BQQXtlnxD4ThtXwwLeQD8+XSrz8AAAA=](https://carlosmpv.github.io/quickshare-md/?q=H4sIAAAAAAAAAxXKwQ2AMAgF0LtT/MSR7AJISW2kpRE4uL3xnd+Og8ZSgee5qMlWru5gS60gDmi/BQQXtlnxD4ThtXwwLeQD8+XSrz8AAAA=)
* Although rendered content is sanitized, **this project is not hardened for production use**.


## Disclaimer
This is a toy project intended for experimentation and learning purposes.
Do not use it to store sensitive information.

