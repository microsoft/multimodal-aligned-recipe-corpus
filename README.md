# Microsoft Research Multimodal Aligned Recipe Corpus

This repository contains information about how to access the dataset described in the paper below:

<a href="https://aclanthology.org/2020.acl-main.440/">A Recipe for Creating Multimodal Aligned Datasets for Sequential Tasks</a><br/>
<i>In the proceedings of Association of Computational Linguistics ACL2020 </i><br/>
Angela S. Lin, Sudha Rao, Asli Celikyilmaz, Elnaz Nouri, Chris Brockett, Debadeepta Dey, Bill Dolan <br/>
Microsoft Research, Redmond, WA, USA <br/>

Contact Person: Sudha Rao (Sudha.Rao@microsoft.com)

# Steps for downloading the corpus

pip install azure-storage-blob

Run the following in a python3 environment: 

from azure.storage.blob import BlobClient <br/>
blob_client = BlobClient.from_blob_url(blob_url="https://recipecorpus.z13.web.core.windows.net/multimodal-aligned-recipe-corpus.zip") <br/>
with open("./multimodal-aligned-recipe-corpus.zip", "wb") as my_blob: <br/>
&emsp;&emsp;blob_data = blob_client.download_blob() <br/>
&emsp;&emsp;blob_data.readinto(my_blob) <br/>

Running this should download the zipped file (multimodal-aligned-recipe-corpus.zip) to the current directory. 

Read multimodal-aligned-recipe-corpus/README.txt for further details about the format of the data. 

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
