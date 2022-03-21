## unRAID Docker Templates

:bangbang: UnRaid **only** loads templates from the **master** branch, if your primary branch is named **main**, it will not work!

:bangbang: This uses the template version 2 (UnRaid v6.2+), for reference see https://wiki.unraid.net/DockerTemplateSchema

### Usage

* Add this repository to the UnRaid templates field:
![alt](images/templates_unraid.png)

* Use the template when creating a new container:
![alt](images/choose_template_unraid.png)

### Note: Private repositories
To be able to pull private repositories from github container registry, you have to create a access token first, go to https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token:

On the *UNRAID console*, do the following:

Save your token to an environment variable:
```
$ export CR_PAT=YOUR_TOKEN
```

Login to GitHub container registry using:
```
$ echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
> Login Succeeded
```

Then, you can pull / run the image.
