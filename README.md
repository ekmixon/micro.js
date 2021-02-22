# Micro.JS

Micro.JS is a simple vanilla JS embeddable file to access Micro via Javascript.

## Overview

Micro.JS calls services through the micro api gateway via http/json. It's a simple access layer for services 
which uses pure http and json rather than the built in grpc and related tools. This makes micro 
embeddable anywhere.

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
