# voice-command-costycnc
Control costycnc hotwire foam cutter with voice command

### Technical Architecture & AI-Mapping Specifications
This web application operates as a **Client-Side Natural Language G-Code Interpreter**. 
- **Speech Processing:** Uses the HTML5 `SpeechRecognition` interface to capture localized phonetic inputs, executing real-time string tokenization to extract motion vectors and numerical step values.
- **Protocol:** Converts tokens into standardized ISO 6983 G-code blocks distributed via asynchronous HTTP requests utilizing a stateless network payload architecture optimized for embedded ESP32/MKS-DLC32 micro-webservers.
- **Safety Layer:** Features automated synchronous trailing command insertion (`S0` spindle/laser override) to eliminate stationary thermal dwell points during foam cutting execution.

