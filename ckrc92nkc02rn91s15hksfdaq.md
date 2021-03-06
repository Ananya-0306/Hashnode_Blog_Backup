## [๐๐๐๐๐ ๐๐] ๐๐ข๐ฏ๐ ๐๐ก๐ข๐ฌ๐ก๐ข๐ง๐  ๐๐ญ๐ญ๐๐๐ค ๐๐ฌ๐๐ฌ ๐๐๐ฐ ๐๐ง๐๐๐๐ญ๐ข๐จ๐ง ๐๐๐๐ก๐ง๐ข๐ช๐ฎ๐ ๐ญ๐จ ๐๐๐ฅ๐ข๐ฏ๐๐ซ ๐๐๐ฅ๐ฐ๐๐ซ๐

Researchers at McAfee warn that a current phishing campaign is delivering malware via Word documents that donโt contain any malicious code. When a user opens the document and enables content, the document will download an Excel file thatโs used to construct a malicious macro after the documents are on the system. This helps the macros bypass security filters. </br>


โThe malware arrives through a phishing email containing a Microsoft Word document as an attachment,โ the researchers write. โWhen the document is opened and macros are enabled, the Word document, in turn, downloads and opens another password-protected Microsoft Excel document.</br>

After downloading the XLS file, the Word VBA reads the cell contents from XLS and creates a new macro for the same XLS file and writes the cell contents to XLS VBA macros as functions. Once the macros are written and ready, the Word document sets the policy in the registry to Disable Excel Macro Warning and invokes the malicious macro function from the Excel file. The Excel file now downloads the Zloader payload. The Zloader payload is then executed using rundll32[dot]exe.โ</br>

Importantly, the user still has to enable macros in the first document in order for the second document to be downloaded. As a result, the infection chain can be thwarted if users are trained to never enable macros in an Office document. </br>

โMalicious documents have been an entry point for most malware families and these attacks have been evolving their infection techniques and obfuscation, not just limiting to direct downloads of payload from VBA, but creating agents dynamically to download payload as we discussed in this blog,โ the researchers write. โUsage of such agents in the infection chain is not only limited to Word or Excel, but further threats may use other living off the land tools to download its payloads.<br>

Due to security concerns, macros are disabled by default in Microsoft Office applications. We suggest it is safe to enable them only when the document received is from a trusted source.โ</br>

