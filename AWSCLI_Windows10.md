### Download AWSCLI

- Download the latest stable version of [AWSCLI for Windows msi](https://awscli.amazonaws.com/AWSCLIV2.msi) and extract the contents.
- File Name - AWSCLIV2.msi

### Set the environment variable
- Copy the absolute path folder under the downloaded kubectl.exe
  e.g., C:/Dashboard/AWSCLIV2.msi
- In the Search on the taskbar, look and open "Edit environment variables for my account".
- Under User variables, edit `path` environment variable and add a new entry pointing to the Daseboard folder as copied above. Save the entries.

### Test AWSCLI
- Open command prompt and run ` awscli`.
- To Check the version, run `aws --version`
