# Creating a document in Captain

A document in Captain acts as a knowledge resource for the assistant. By linking your help center or guides, Captain can analyze the content and effectively assist with customer inquiries.

Currently, we support website URLs and PDF files as sources , but we’re planning to expand this to include Notion documents in the future.

## How to create a document?

On the sidebar menu, click on the **Documents** option under Captain. You will see a page like the one below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT3FlQ2dFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--c9601a874ca435ff3d4d6092ba71b05a4f2caf10/document-1.png)

By clicking on **Create a New Document**, you will be presented with a form where you can either enter the URL of your knowledge base or upload a PDF file. Note that we only support public URLs at the moment.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCTllybmdJPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7647cf49d214367b6d03c75a52b4639b855539df/image.png)

Once you’ve entered the URL of your knowledge base or help center or uploaded a document, click on **Create** to start the process. Captain will begin analyzing the content from the provided URL or document, using it as a starting point to gather information that can help answer customer questions effectively.

Captain will systematically crawl all pages linked under the provided URL path, scanning for articles, guides, and other resources associated with the main URL. For instance, if you provide a URL like <https://chatwoot.help/user-guide>, Captain will analyze all URLs that start with this path. As it crawls the content, it organizes and indexes the information, making it easily accessible for answering customer inquiries. This structured crawling process guarantees that all relevant knowledge from your specified source is captured and available for reference.

For PDF uploads, Captain will extract and analyze the text content from the file. This is useful for adding product manuals, guides, or any other documentation stored as PDFs to your knowledge base.

The document will be generated, and any newly identified documents during the crawling will also be added individually as separate documents.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSHVnQ2dFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--15d49fb87e3807c7d30c0995073495392d885afc/document-3.png)

If you wish to remove a specific document that is not relevant, you can delete it. This will also erase all the associated information Captain has collected from that document, and ensures it is no longer referenced in any conversations.

## How can I verify that the content is properly parsed?

To ensure that the content is properly parsed, Captain analyzes the provided documents to identify potential questions. It then generates a list of FAQs related to the document. By reviewing these FAQs, you can verify that the content has been accurately processed and correctly interpreted.

You can view the FAQs generated for each document. Simply click on the three-dot menu in the document and choose **View** **Related Responses** to access them.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCT2VnQ2dFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--e58a2d54530aecaf48c4fbbd640d0694084592be/document-4.png)

This will display the related FAQs, as shown below.

![](https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBCSXFoQ2dFPSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--7264180404b6ac1d1b5533d674bc040f7a2db0fa/document-5.png)

## Usage limit

If you haven’t subscribed to a paid add-on for Captain, the number of documents you can add will be limited. With the Startups plan, you can add up to 100 documents for free. For higher plans, the limit increases to 200 free documents with the Business plan and 300 free documents with the Enterprise plan.
