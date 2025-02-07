# Open OnDemand MATLAB App for Delta

Interactive MATLAB app for Delta's Open OnDemand portal

## Requirements

On compute nodes (NOT the Open OnDemand node):

 - MATLAB (license optional)
   - This app will use a license file if it's specified via `MLM_LICENSE_FILE`, but users also have the option to log in and use their own license
 - [Lmod](https://www.tacc.utexas.edu/research-development/tacc-projects/lmod) and relevant modules for MATLAB
 - Apptainer

## Installation

 1. Clone this app to OOD's app directory (/var/www/ood/apps/sys by default).
 2. Adjust repo URLs in `container_files/matlab-proxy.def` to use correct local or external repos
 3. Build the Apptainer image and place it into a path that matches the command in `template/script.sh.erb`.
 4. Adjust cluster name and Lmod module names in form.yml to match the system.

## Acknowledgements

 - [OSC/bc_osc_jupyter](https://github.com/OSC/bc_osc_jupyter)
 - [matlab-proxy](https://github.com/mathworks/matlab-proxy)
