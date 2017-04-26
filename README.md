ansible-role-repo-elrepo
===============

Sets up the ELRepo repo on RHEL/CentOS

Requirements
------------

None

Role Variables
--------------
    elrepo_repo_version: "7.0-2"
    elrepo_repo_url: "https://elrepo.org/linux/elrepo/el{{ ansible_distribution_major_version }}/{{ ansible_architecture }}/RPMS/elrepo-release-{{ elrepo_repo_version }}.el{{ ansible_distribution_major_version }}.elrepo.noarch.rpm"
    elrepo_repo_gpg_key_url: "/etc/pki/rpm-gpg/RPM-GPG-KEY-elrepo.org"
    elrepo_repofile_path: "/etc/yum.repos.d/elrepo.repo"
    elrepo_repo_disabled: true

Dependencies
------------

None

Example Playbook
----------------

    - hosts:
        - centos
      roles:
        - ansible-role-repo-elrepo

License
-------

MIT

Author Information
------------------

rmacdonald@nexcess.net
