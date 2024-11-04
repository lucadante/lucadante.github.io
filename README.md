<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DocsBot AI Chatbot</title>
</head>
<body>
    <h1>Welcome to the DocsBot AI Chatbot</h1>
    <p>This page contains the embedded DocsBot AI chatbot.</p>

    <!-- Container for the DocsBot AI chatbot -->
    <div id="docsbotai-root"></div>

    <!-- DocsBot AI embed code -->
    <script type="text/javascript">
        window.DocsBotAI = window.DocsBotAI || {};
        DocsBotAI.init = function(e) {
            return new Promise((t, r) => {
                var n = document.createElement("script");
                n.type = "text/javascript";
                n.async = true;
                n.src = "https://widget.docsbot.ai/chat.js";
                let o = document.getElementsByTagName("script")[0];
                o.parentNode.insertBefore(n, o);
                n.addEventListener("load", () => {
                    let n;
                    Promise.all([
                        new Promise((t, r) => {
                            window.DocsBotAI.mount(Object.assign({}, e)).then(t).catch(r)
                        }),
                        (n = function e(t) {
                            return new Promise(e => {
                                if (document.querySelector(t)) return e(document.querySelector(t));
                                let r = new MutationObserver(n => {
                                    if (document.querySelector(t)) return e(document.querySelector(t)), r.disconnect()
                                });
                                r.observe(document.body, { childList: true, subtree: true })
                            })
                        })("#docsbotai-root"),
                    ]).then(() => t()).catch(r)
                });
                n.addEventListener("error", e => { r(e.message) })
            })
        };

        DocsBotAI.init({ id: "cTW2YtLwX3hKtkVwhgJJ/QPMD7vaceBMPeBHfKr02" });
    </script>
</body>
</html>
