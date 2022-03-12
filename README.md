# action-jdk-sbt-cache

Checkout Code, Setup JDK and SBT Cache by SO in one step

## Usage

```yaml

#... run config ...

jobs:
  name-job:
    runs-on: ubuntu-latest
    steps:
      # Add like first step
      - name: Checkout / Setup JDK / SBT-Cache
        uses: rodobarcaaa/action-jdk-sbt-cache@v1.0.0
        with:
          token: ${{ secrets.REPO_GITHUB_TOKEN }}

      #... next steps ...     

```

## Configuration

The following inputs are available (some of them are optional):

| Input (click on name for description)                                                                                                     |                      Allowed values                      | Default | Required
|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------:|:-------:|:---------:|
| <details><summary>`token`</summary><br/>Github Personal Access Token with permission on repo (or `${{ secrets.GITHUB_TOKEN }}`)</details> | Valid [Github Token](https://github.com/settings/tokens) |    -    |    yes
| <summary>`fetch-depth`</summary>                                                                                                          |   Like [Checkout](https://github.com/actions/checkout)   |    1    |    no
| <summary>`jdk-distro`</summary>                                                                                                           | Like [Setup-Java](https://github.com/actions/setup-java) |  adopt   |    no
| <summary>`jdk-version`</summary>                                                                                                          | Like [Setup-Java](https://github.com/actions/setup-java) |    8    |    no    

