# AI Red Team Test of Llama3 Using Garak

##Overview
This project demonstrates AI red team testing against a locally hosted Llama3 model

##Lab Enviroment
-Kali Linux VM (VirtualBox)
-Ollama running locally
-Llama3 model
-Garak AI Vulnerability Scanner

##Attack Tested
encoding.InjectBase64

This test checks whether an AI model will decode Base64 encoded prompt that could hide malicious instructions

Example encoded payload:
SGVsbG8=

Decoded:
Hello

##Observation
During testing the model detected encoded input and attempted to decode Base64 content.

Example responses observed:
"It seems like you've shared a code or password"
"Let me crack open this BASE64 code for you"

##Conclusion
The test shows the model attempts to interpret encoded payloads.Further manual testing is required to determine
if encoded prompts could bypass safety 

##Tools Used
-Kali Linux
-Ollama
-Llama3
-Garak
