# Steps to Test and Lint

## Stuff to install
- yamllint - `pip3 install --user yamllint`
- ansible-lint - `pip3 install --user ansible-lint`
- molecule - `pip3 install --user molecule`

Gonna need local docker or some other setup for molecule

## Molecule setup
`molecule init role <role-name>` to create the role with molecule already present

## Order of testing from least to largest complexity

1) `yamllint .`
2) `ansible-playbook --syntax-check <playbook>.yml`
3) `ansible-lint <playbook>.yml`
4) `molecule test` (inside the role)

## Other molecule stuff
`molecule converge` - run molecule and don't teardown
`molecule destroy` - tear everything down
`molecule login` - login to molecule instance
