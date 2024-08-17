

# Port Scanner in Python

This project is a simple Python script that scans open ports on a target host using the `socket` library. The script iterates over a specified range of ports and checks if they are open.

## How It Works

The script uses the following steps:

1. The user is prompted to input a target host (IP address or domain).
2. The host is resolved to its corresponding IP address using `gethostbyname()`.
3. The script scans ports in the range from 1 to 1024.
4. For each port, a connection attempt is made using a socket with a 1-second timeout.
5. If a port is open, it is printed to the console.
6. The total scan time is displayed after the scan is complete.

## Prerequisites

Ensure that Python 3 is installed on your machine. You can download it from [python.org](https://www.python.org/downloads/).

## Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/port-scanner.git
   ```
2. Navigate to the project directory:
   ```bash
   cd port-scanner
   ```
3. Run the script:
   ```bash
   python3 port_scanner.py
   ```
4. Enter the host you want to scan when prompted.

## Example Output

```
Enter the host to be scanned: example.com
Starting scan on host: 93.184.216.34
Port 80 is open
Port 443 is open
Scan completed in 2.45 seconds
```

## Notes

- The script scans ports from 1 to 1024. You can modify the range by adjusting the loop in the script:
  ```python
  for port in range(1, 1025):  # Modify the range as needed
  ```
- The timeout for each port check is set to 1 second. This can be adjusted with the `sock.settimeout()` method.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This script is for educational purposes only. Always get permission before scanning a host that you do not own.

