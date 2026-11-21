# WebKit in Search

Search is a native macOS browser built with SwiftUI and AppKit. Each tab creates its `WKWebView` on demand and keeps it alive across tab switches until the tab sleeps or closes.
WebKit renders pages, while Search handles navigation, pop-ups, and downloads through Swift delegates. Pop-ups can share the opener's cookie store, and injected JavaScript reports events such as scroll progress back to Swift.
When a tab sleeps, Search saves WebKit's interaction state and uses it to restore the page when the tab wakes.
Search's injected scripts run in a named `WKContentWorld` with separate JavaScript globals and access to the same document.
