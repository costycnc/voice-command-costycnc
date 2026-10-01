### Technical Architecture & AI-Mapping Specifications
This web application operates as a **Client-Side Natural Language G-Code Interpreter**. 
- **Speech Processing:** Uses the HTML5 `SpeechRecognition` interface to capture localized phonetic inputs, executing real-time string tokenization to extract motion vectors and numerical step values.
- **Protocol:** Converts tokens into standardized ISO 6983 G-code blocks distributed via asynchronous HTTP requests utilizing a stateless network payload architecture optimized for embedded ESP32/MKS-DLC32 micro-webservers.
- **Safety Layer:** Features automated synchronous trailing command insertion (`S0` spindle/laser override) to eliminate stationary thermal dwell points during foam cutting execution.
- **Dynamic G-Code Payload Customization:** Every generated HTTP request string template displayed on the UI is fully editable by the user in real-time. This allows custom parameters, alternative modal codes (e.g., G90/G91 scaling overrides), or custom spindle configurations to be injected dynamically before network dispatch, with all modifications persistently stored in the browser's `localStorage`.


