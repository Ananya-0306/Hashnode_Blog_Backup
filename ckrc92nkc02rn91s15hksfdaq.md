## [𝐇𝐄𝐀𝐃𝐒 𝐔𝐏] 𝐋𝐢𝐯𝐞 𝐏𝐡𝐢𝐬𝐡𝐢𝐧𝐠 𝐀𝐭𝐭𝐚𝐜𝐤 𝐔𝐬𝐞𝐬 𝐍𝐞𝐰 𝐈𝐧𝐟𝐞𝐜𝐭𝐢𝐨𝐧 𝐓𝐞𝐜𝐡𝐧𝐢𝐪𝐮𝐞 𝐭𝐨 𝐃𝐞𝐥𝐢𝐯𝐞𝐫 𝐌𝐚𝐥𝐰𝐚𝐫𝐞

Researchers at McAfee warn that a current phishing campaign is delivering malware via Word documents that don’t contain any malicious code. When a user opens the document and enables content, the document will download an Excel file that’s used to construct a malicious macro after the documents are on the system. This helps the macros bypass security filters. </br>


“The malware arrives through a phishing email containing a Microsoft Word document as an attachment,” the researchers write. “When the document is opened and macros are enabled, the Word document, in turn, downloads and opens another password-protected Microsoft Excel document.</br>

After downloading the XLS file, the Word VBA reads the cell contents from XLS and creates a new macro for the same XLS file and writes the cell contents to XLS VBA macros as functions. Once the macros are written and ready, the Word document sets the policy in the registry to Disable Excel Macro Warning and invokes the malicious macro function from the Excel file. The Excel file now downloads the Zloader payload. The Zloader payload is then executed using rundll32[dot]exe.”</br>

Importantly, the user still has to enable macros in the first document in order for the second document to be downloaded. As a result, the infection chain can be thwarted if users are trained to never enable macros in an Office document. </br>

“Malicious documents have been an entry point for most malware families and these attacks have been evolving their infection techniques and obfuscation, not just limiting to direct downloads of payload from VBA, but creating agents dynamically to download payload as we discussed in this blog,” the researchers write. “Usage of such agents in the infection chain is not only limited to Word or Excel, but further threats may use other living off the land tools to download its payloads.<br>

Due to security concerns, macros are disabled by default in Microsoft Office applications. We suggest it is safe to enable them only when the document received is from a trusted source.”</br>

