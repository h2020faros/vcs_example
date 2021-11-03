# VCS Example
VCS can be used to clone multiple projects from a list of repositories. 

## Installation
To install, run
```shell
sudo apt install python3-vcstool
```

## Usage
- Create `YAML` type file to list repositores. See [repos.yml](./repos.yml)
- Clone the content
```shell
mkdir -p vcs_example_ws/src
wget wget https://raw.githubusercontent.com/h2020faros/vcs_tool_example/main/repos.yml -P vcs_example_ws
vcs import vcs_example_ws/src < vcs_example_ws/repos.yml
```
- Check everything got cloned
```shell
ls vcs_example_ws/src
```
- Possibly install dependencies via [rosdep](https://docs.ros.org/en/crystal/Installation/Linux-Install-Binary.html#installing-and-initializing-rosdep)
```shell
cd vcs_example_ws
rosdep install --from-paths src --ignore-src -r -y
```
- Build
```shell
colcon build
```


## Links
- [Foxy source checkout](https://docs.ros.org/en/foxy/Installation/Maintaining-a-Source-Checkout.html)
- [VCS Tool Github](https://github.com/dirk-thomas/vcstool)

