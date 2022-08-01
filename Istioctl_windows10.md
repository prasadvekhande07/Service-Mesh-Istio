### Download Istio

- Download the latest stable version of [Istio for windows zip](https://github.com/istio/istio/releases) and extract the contents.
- File Name - istio-1.13.6-win.zip

### Unzip file istio-1.13.6-win.zip
- Rename folder istio-1.12.9-win to istio-1.13.6
- Copy folder istio-1.13.6 to Download folder
- Copy path upto bin foler like C:/Dashboard/istio-1.13.6/bin

### Set the environment variable
- Copy the absolute path to the `bin` folder under the downloaded istio-<VERSION_NUMBER> folder
  e.g., C:/Dashboard/istio-istio-1.13.6/bin
- In the Search on the taskbar, look and open "Edit environment variables for my account".
- Under System variables, edit `path` environment variable and add a new entry pointing to the bin folder as copied above. Save the entries.

### Test Istioctl
- Open command prompt and run ` istioctl`.
- To Check the version, run `istioctl version`
