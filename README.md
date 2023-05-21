# Power BI Log Analytics Template Reports

ERIN's VERSION 

Power BI allows users to configure connections to Azure Log Analytics where they can retain detailed historical activity data.
This repo hosts Power BI Template (.pbit) reports that you can point to your Azure Log Analytics workspaces to load data and get inisights right away! 

After opening the template you will be prompted to enter your Log Analytics Workspace ID. Once it has this information and you have logged in to Azure, the report can refresh. 

Here are the available templates:

- **Log Analytics for Analysis Services Engine:** This report allows you to visualize the activity of datasets hosted in the Analysis Services Engine in Power BI workspaces. You can use it to identify load patterns, investigate user actions, look at query performance trends, visualize refreshes, and much more! 



## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.

## Known Issues
- SE Duration measures are currently blank. This is because Vertipaq Storage Engine events are not yet supported in the Preview.
- If you find the report takes a very long time to refresh and appears to be stuck, try to load a shorter period of time. We have built the Power Query logic with Log analytics Query limits in mind, but it is possible you are hitting limits. Another thing to try is to go to the Regional Settings -> Locale in the template and change it to US date format. We have had reports of European customers having the report load blocked becuase of date conversion errors.
