

**README.md**

## Scapy Packet Sniffer

This script demonstrates live network traffic sniffing using the Scapy library in Python. It captures packets, extracts source and destination IPs, protocol information, and attempts to decode the payload for TCP and UDP packets.

**Requirements**

  * Python 3 ([https://www.python.org/](https://www.google.com/url?sa=E&source=gmail&q=https://www.python.org/))
  * Scapy library (installation: `pip install scapy`)

**Running the Script**

1.  **Save the script:** Save the code as `packet_sniffer.py` or a preferred filename.

2.  **Run the script:** Open a terminal or command prompt, navigate to the directory where you saved the script, and run the following command:

    ```bash
    python packet_sniffer.py
    ```

**Functionality**

The script continuously captures network packets on the default interface and analyzes them using Scapy:

  * **IP Layer:** Checks if the packet has an IP layer. If so, it extracts the source IP, destination IP, and protocol type (TCP, UDP, etc.).
  * **TCP Payload:** If the protocol is TCP, it tries to access the Raw layer and decode the payload as UTF-8. If decoding fails (e.g., due to non-text data), it prints an error message.
  * **UDP Payload:** Similar to TCP, for UDP packets, it attempts to decode the Raw layer payload as UTF-8 and prints it or an error message if decoding fails.

**Important Notes**

  * **Live Network Traffic:** This script captures live network traffic on your default network interface. It might reveal sensitive information passing through the network. Use it responsibly and in an environment where you have appropriate permissions.
  * **Limited Payload Decoding:** The script attempts to decode the payload as UTF-8, but it might not always be accurate. Non-text data or invalid UTF-8 will likely cause decoding errors.
  * **Ethical Considerations:** Network sniffing has ethical implications. Ensure you have permission to capture traffic on the network you're using.

**Stopping the Sniffer**

To stop the sniffer, press `Ctrl+C` in the terminal window where you ran the script.

**Disclaimer**

This script is intended for educational purposes only. Be responsible and ethical when using it. It is important to understand your local laws and network policies regarding network sniffing.
