# cfmu-player-test
A stripped down version of CFMU's player to use for debugging.


## Instructions
Step 1:
```
$: git clone https://github.com/aenoble/cfmu-player-test.git
```
Step 2:
Open index.html in web browser


## Issues
1.  CFMU tracks stop transferring part way through.
  * Possible reason: "Keep-Alive:timeout=5, max=100" + "Connection: Keep Alive" in Response header
2.  CFMU tracks don't allow range tracking.
  * Possible reason: "Accept-Ranges:bytes" + "Access-Control-Allow-Headers:range, accept-encoding" **NOT** in Response header.
