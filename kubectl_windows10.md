### Download Kubectl

- Download the latest stable version of [Kubectl for Windows exe](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/) and extract the contents.
- File Name - kubectl.exe
- Example - curl -LO "https://dl.k8s.io/release/v1.24.0/bin/windows/amd64/kubectl.exe"

### Set the environment variable
- Copy the absolute path folder under the downloaded kubectl.exe
  e.g., C:/Dashboard/kubectl.exe
- In the Search on the taskbar, look and open "Edit environment variables for my account".
- Under User variables, edit `path` environment variable and add a new entry pointing to the Daseboard folder as copied above. Save the entries.

### Test Istioctl
- Open command prompt and run ` kubectl`.
- To Check the version, run `kubectl version --client`
