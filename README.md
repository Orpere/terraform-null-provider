#terraform-null-provider -> repo that you can use to see how null provider work

## how can I use this repository?

This repo has as dependencies a command line or shell git and terraform.You can find the install instructions bellow on [EXTRAS](#extras) section.

## How can I use this repo`?`

### Task - clone repo terraform-null-provider

- open your shell or command line and go to the directory where you pretend to add the repo

```bash
cd <directory where pretend to add the repo>
```

```git
git clone git@github.com:Orpere/terraform-null-provider.git
```

### Task - move to your repo folder

```bash
cd terraform-null-provider
```
## Task - terraform init

- this will retrieve all dependencies for terraform scripts

```terraform
terraform init
```

### Task - run terraform apply

```terraform
terraform apply
```

- This step will prompt <<Do you want to perform these actions?>>
  the answer should be **yes** 

 

### Task - check the result of the null provider

- In this case should be

```terraform 
random_pet.example: Creating...
random_pet.example: Creation complete after 0s [id=stirring-manatee]
null_resource.example: Creating...
null_resource.example: Provisioning with 'local-exec'...
null_resource.example (local-exec): Executing: ["/bin/sh" "-c" "echo stirring-manatee"]
null_resource.example (local-exec): stirring-manatee
null_resource.example: Creation complete after 0s [id=1994326005307348540]

Apply complete! Resources: 2 added, 0 changed, 0 destroyed.
```

### Task - Terraform destroy

```terraform
terraform destroy
```

- This will request confirmation and if your answer is **yes**
- this will wipe the resources you have builded

#### EXTRAS

This repo was based on the [documentation](https://www.terraform.io/docs/providers/null/index.html)

[Install git](https://gist.github.com/derhuerst/1b15ff4652a867391f03#file-intro-md)
for more instructions to use git you can check the [link](https://rogerdudler.github.io/git-guide/) it will have a much better explanation about all git steps

After clone the repo you can install terraform downloading the adequate version to your OS on [Terraform](https://www.terraform.io/downloads.html)
If you don't know how to install please follow the [tutorial](https://learn.hashicorp.com/terraform/getting-started/install.html)