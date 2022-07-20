### Download Istio

- Download the latest stable version of [Istio for windows zip](https://github.com/istio/istio/releases) and extract the contents.
- File Name - istio-1.12.9-win.zip

### Unzip file istio-1.12.9-win.zip
- Rename folder istio-1.12.9-win to istio-1.12.9
- Copy path upto bin foler like C:/Dashboard/istio-1.12.9-win/bin

### Set the environment variable
- Copy the absolute path to the `bin` folder under the downloaded istio-<VERSION_NUMBER> folder
  e.g., C:/Dashboard/istio-1.0.5-win/istio-1.0.5/bin
- In the Search on the taskbar, look and open "Edit environment variables for my account".
- Under User variables, edit `path` environment variable and add a new entry pointing to the bin folder as copied above. Save the entries.

### Test Istioctl
- Open command prompt and run ` istioctl`.
- To Check the version, run `istioctl version`
