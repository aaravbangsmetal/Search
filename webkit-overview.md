# WebKit in Search

Search is a native macOS browser built with SwiftUI and AppKit. Each tab creates its `WKWebView` on demand and keeps it alive across tab switches until the tab sleeps or closes.
WebKit renders pages, while Search handles navigation, pop-ups, and downloads through Swift delegates. Pop-ups can share the opener's cookie store, and injected JavaScript reports events such as scroll progress back to Swift.
