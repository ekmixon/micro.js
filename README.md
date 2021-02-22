# Micro.JS

Micro.JS is a simple vanilla JS embeddable file to access Micro via Javascript.

## Usage

Assuming the service "helloworld" is running on Micro in the default "micro" namespace.

```js
document.addEventListener("DOMContentLoaded", function (event) {
    document.getElementById("btn").onclick = function () {
        Micro.post(
        "helloworld/call",
            "micro",
            {
                name: "Joe",
            },
            function (data) {
                alert(JSON.stringify(data))
            }
        );
    }
});
```
