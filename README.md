Ansible Role: Intel_SGX_DNNL
=========

Ansible Role to build and install the Intel SGX DNNL library from source which is a patched version of the [oneDNN](https://github.com/oneapi-src/oneDNN) library.

Requirements
------------

Pre-requisites not be covered by Ansible or the role:
- Build-essentials for building the libraries from source

Role Variables
--------------

The variables defined in `defaults/main.yml` file describe the base URL download locations.

The entries in `vars/main.yml` can be used to change the checkout version of the SGX-Linux repo.

Dependencies
------------

Roles hosted on Galaxy and their parameters:
- melhindi.intel_sgx_pws
- melhindi.intel_sgx_sdk

Use the following command to install these dependencies:
`ansible-galaxy install -r requirements.yml`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: melhindi.intel_sgx_dnnl }

License
-------

Apache 2.0

Contribute
-------

To contribute to the development of this role the following setup is recommended:

```
# 1. Clone the repository with the expected role name:
git clone git@github.com:melhindi/ansible-role-intel-sgx-dnnl.git melhindi.intel_sgx_dnnl

# 2. Initialize the virtual environment
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt

# 3. Use molecule to test the role
molecule converge
```
*Note*: This setup assumes that you do not have any globally installed ansible or molecule. Sometimes globally installed ansible/molecule can cause package/dependency conflicts.
