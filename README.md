<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DocsBot AI Chatbot</title>
    <style>
        /* Style to center the chatbot container */
        #docsbotai-root {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80%;  /* Adjust width as needed */
            height: 80%; /* Adjust height as needed */
            z-index: 1000;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            background-color: #ffffff;
            border-radius: 8px;
            overflow: hidden;
        }

        /* Full-screen overlay background */
        #overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 999;
        }
    </style>
</head>
<body>
    <!-- Full-screen overlay background -->
    <div id="overlay"></div>

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

        DocsBotAI.init({ id: "cTW2YtLwX3hKtkVwhgJJ/QPMD7vaceBMPeBHfKr02" }).then(() => {
            // Delay to ensure the chatbot icon is present in the DOM
            setTimeout(() => {
                const chatbotIcon = document.querySelector(".docsbotai-icon"); // Adjust selector if necessary
                if (chatbotIcon) {
                    chatbotIcon.click(); // Simulate a click on the icon
                }
            }, 1000); // Adjust the delay as needed to ensure the icon is loaded
        });
    </script>

    <script>
        // JavaScript to close the overlay and chatbot when clicking outside
        document.getElementById('overlay').addEventListener('click', function() {
            document.getElementById('docsbotai-root').style.display = 'none';
            document.getElementById('overlay').style.display = 'none';
        });
    </script>
</body>
</html>
