The workerd runtime appears to be causing a single GET request to /blog to be transmitted over 147 TCP packets, most of them containing single bytes. 


build
```
npm run build
```

run on PORT 8788
```
npm run preview:wrangler
```

check wireshark:

![image](https://github.com/user-attachments/assets/02ab98ea-92d3-4432-8a3d-88fd64ad0ccc)

click "follow TCP stream"

![image](https://github.com/user-attachments/assets/33f291bb-2cda-4a2d-9685-d9aa36457914)

notice the number of packets making up this GET to /blog


<img width="339" alt="image" src="https://github.com/user-attachments/assets/25d9cc6e-90c7-4b50-956a-a7e5862dc495">

compare with the default astro runtime by running `npm run dev` and doing the same:

