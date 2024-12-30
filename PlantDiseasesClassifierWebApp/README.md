First, clone this repository into your environment. To use the app, navigate to the appsettings.json file and fill in the required information from the Azure Custom Vision API as follows:

<image>


{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*",
  "AzureVisionSettings": {
    "PredictionKey": "",
    "Endpoint": "",
    "ProjectId": "",
    "PublishedModelName": ""
  }
}

To obtain this information, go to the project portal in the Custom Vision portal and click on the settings icon.

*Endpoint*:  This should look something like "https://name-of-your-azureai-services-instance.cognitiveservices.azure.com/"

*ProjectId*: You can find this in the Custom Vision portal under Settings, or extract it from the URL.

*PublishedModelName:* This is the name you assigned when publishing the model. For example, it might be paddydoctor-quick-training.

To run your application in Visual Studio Code, follow these steps:

1. **Open the Project**:
   - Open Visual Studio Code.
   - Use `File > Open Folder` and select the root folder of your project (`PlantDiseasesClassifierWebAppOrg`).

2. **Install Dependencies**:
   - Open the terminal in VS Code (`Ctrl + `).
   - Run the following command to restore the NuGet packages:
     ```sh
     dotnet restore
     ```

3. **Build the Project**:
   - In the terminal, run the following command to build the project:
     ```sh
     dotnet build
     ```

4. **Run the Project**:
   - In the terminal, run the following command to start the application:
     ```sh
     dotnet run --project PlantDiseasesClassifierWebApp/PlantDiseasesClassifierWebApp.csproj
     ```

5. **Open in Browser**:
   - Once the application is running, it will display the URLs where the application is hosted (e.g., `http://localhost:5167` or `https://localhost:7002`).
   - Open your web browser and navigate to one of these URLs.

If you encounter any issues, alternatively, you can specify the project file directly:

`dotnet run --project C:\Users\hzmarrou\OneDrive\azopenai\plant-diseases-classifier-webapp\PlantDiseasesClassifierWebApp\PlantDiseasesClassifierWebApp.csproj`