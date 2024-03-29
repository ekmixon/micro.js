# Micro.js

Micro.js is a simple vanilla javascript embeddable file to access Micro via Javascript.

## Overview

Micro.js calls services through the micro api gateway via http/json. It's a simple access layer for services 
which uses pure http and json rather than the built in grpc and related tools. This makes micro 
embeddable anywhere.

## Usage

Assuming the service "helloworld" is running on Micro in the default "micro" namespace.

Import the script

```js
<script src="https://raw.githubusercontent.com/micro/micro.js/master/index.js" /><script>
```

Copy the below code

```js
document.addEventListener("DOMContentLoaded", function (event) {
    document.getElementById("btn").onclick = function () {
        Micro.post("helloworld/call", "micro",
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
