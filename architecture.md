Auditum is designed to be a modular layered tool. The idea is to have multiple **Scraping Modules** and **IO Modules** connected by the **Controller Module**.

# Scraping Modules

This module patten has the responsibility of **searching** documents about a particular technology, framework or language. When searching for keywords, the acquired HTML content must be parsed to the **MarkDown** format, and after that be sent to the **Controller Module** to be stored.

# IO Modules

This module pattern has the responsibility of **Interacting with the final user**. It must receive text commands in a specific chat platform and send the raw commands to the **Controller Module**. The content received from the **Controller Module** must be parsed in text formats that are supported by the current chat platform, and then sent to the final.

# Controller Module

Different of the **IO Modules** and **Scraping Modules**, the **Controller Module** must be unique in the entire application and centralize everything into it.
This is the main module of the application, who the other modules should be connected to. This module has the responsibility of store/retrieve the content acquired by the **Scraping Modules**, interpret the commands sent by the **IO Modules** and sending its response.