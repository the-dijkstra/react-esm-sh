# React Islands With no Build Step

This example uses esm.sh/run, a 1KB script allows you to write jsx/tsx in HTML without build! [esm.sh/run](https://github.com/esm-dev/esm.sh/releases/tag/v135)

## How it Works?
After the page loaded, the 1KB tiny script computes the hash of the source of non-javascript <script> elements, then checks the compiled JS exists in the cache, otherwise sends the source code to esm.sh build API and stores it in the cache system.
The cache system includes two iters of storage, are the localStoarge and the Cloudflare Edge network, to make the compiled JS load fast!

![image](https://github.com/the-dijkstra/react-esm-sh/assets/9967336/fa963a17-717b-4e70-8637-6a2a27849215)

## Limitations
There are some limitations you need to be aware of:

- Don't use external imports
- Needs internet connection out of local cache
- Rebuild happens when the HTML changed
