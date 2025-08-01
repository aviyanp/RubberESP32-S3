# RubberESP32-S3
A Rubber Ducky Devboard built around an ESP32-S3-WROOM-1U Module. I built this because I really wanted to make my first devboard and it seemed like the perfect time to do so! It took way too much work, and it costs ~$90 because of Standard PCBA for the ESP32-S3, so I think it'd be better to just buy the parts needed to solder it on by hand and learn all about SMD soldering! It's definitely a learning curve trying to figure out what goes where and how to not screw up your routing so bad that you have to reverse ~4+ hours of work. I'm eventually trying to make an all-in-one mainboard for a robot that would incorporate 4 custom-made motor drivers and an ESP32-S3 controlling it all, so this is the first step in that direction! For now, I wanted something that I can easily test out and use IRL, so I decided to make a rubber ducky! It was really freaking rage-inducing, but it was all good fun and I learned a lot from it all.

---

## Images
![PCB](https://i.ibb.co/B2Nms5VK/Screenshot-2025-07-31-at-10-38-35-PM.png)
![Schematic](https://i.ibb.co/VWwzHV19/Screenshot-2025-07-19-at-9-57-54-AM.png)

---

| Comment               | Designator                | Footprint                       | LCSC     | Quantity | Price (Based on MOQ) | Notes                                                                                                                   |
|-----------------------|---------------------------|---------------------------------|----------|----------|----------------------|-------------------------------------------------------------------------------------------------------------------------|
| 5.1K                  | R12,R13                   | R0603                           | C14677   | 4        | $0.12                |                                                                                                                         |
| 10K                   | R10,R11,R3,R5,R6,R7,R8,R9 | R0603                           | C15401   | 16       | $0.09                |                                                                                                                         |
| 100nF                 | C2,C4                     | C0603                           | C1591    | 4        | $0.28                |                                                                                                                         |
| 1uF                   | C3                        | C0603                           | C1592    | 2        | $0.17                |                                                                                                                         |
| 100R                  | R4                        | R0603                           | C25201   | 2        | $0.1                 |                                                                                                                         |
| 22uF                  | C6                        | CAP-SMD_BD6.3-L6.6-W6.6-FD      | C267472  | 2        | $0.64                |                                                                                                                         |
| TYPE-C 16PIN 2MD(073) | USB1                      | USB-C-SMD_TYPE-C-6PIN-2MD-073   | C2765186 | 2        | $1.1                 |                                                                                                                         |
| 22uF                  | C1                        | C1210                           | C2918511 | 2        | $0.4                 |                                                                                                                         |
| ESP32-S3-MINI-1U      | U1                        | ESP32-S2-MINI-1U                | C2980296 | 3        | $10.8                | I have 3 because I'd otherwise get a $3 fee and it costs around that and it's pretty easy to mess up when soldering it. |
| AMS1117-3.3           | U2                        | SOT-223-3_TabPin2               | C347222  | 2        | $0.2                 |                                                                                                                         |
| TF PUSH               | Card1                     | TF-SMD_TF-PUSH                  | C393941  | 2        | $0.55                |                                                                                                                         |
| SW_SPST               | SW1,SW2                   | SW-SMD_L3.9-W3.0-P4.45          | C455280  | 4        | $0.46                |                                                                                                                         |
| 10uF                  | C5                        | CAP-SMD_BD6.3-L6.6-W6.6-FD      | C72482   | 2        | $0.45                |                                                                                                                         |
| Conn_01x02            | J2                        | PinHeader_1x02_P2.54mm_Vertical |          | 1        | $5.49                | Price includes other headers                                                                                            |
| Conn_01x02            | J1                        | PinHeader_1x02_P2.54mm_Vertical |          | 1        |                      |                                                                                                                         |
| Conn_01x08            | J3                        | PinHeader_1x08_P2.54mm_Vertical |          | 1        |                      |                                                                                                                         |
| Solder Paste          |                           |                                 |          | 1        | $13.95               |                                                                                                                         |
| Solder                |                           |                                 |          | 1        | $8                   |                                                                                                                         |
| PCB                   |                           |                                 |          | 5        | $2                   |                                                                                                                         |
| Stencil               |                           |                                 |          | 1        | $7                   |                                                                                                                         |
| Hotplate              |                           |                                 |          | 1        | $15                  |                                                                                                                         |
| JLCPCB Shipping       |                           |                                 |          |          | $18.63               |                                                                                                                         |
| LCSC Shipping         |                           |                                 |          |          | $10.45               |                                                                                                                         |
| Amazon Shipping       |                           |                                 |          |          | $9                   |                                                                                                                         |

## Total Cost: $104.88
