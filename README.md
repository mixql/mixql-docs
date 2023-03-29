# Build documentation for mixql.org

## Quick build

1. You have [Docker](https://docs.docker.com/desktop/) installed. 
2. Build local Antora builder image
    ```
    mkdir mixql && cd mixql
    git clone https://github.com/mixql/mixql-docs.git
    docker build -t local/antora:lunr -f ./mixql-docs/Dockerfile.lunr .
    ```

3. Generate site by Antora:

   There are two ways to generate site:
   - from local folders (antora-playbook-local.yml) or 
   - from git repos, which will be downloaded grom github (antora-playbook.yml)
   
   Static site will be placed in ./mixql/mixql-docs/public/index.html
    
   3.1. Local sources
   - Download all needed mixql-* repo into ./mixql. Site will be generated in the ./mixql/mixql-docs/public folder.
   
   ```
   git clone https://github.com/mixql/mixql-docs.git   
   git clone https://github.com/mixql/mixql-platform.git
   git clone https://github.com/mixql/mixql-core.git
   git clone https://github.com/mixql/mixql-test-env.git
   ```
   - Generate site via local antora-playbook-local.yml

    ```
    docker run -v $PWD:/antora --rm -t local/antora:lunr --extension @antora/lunr-extension  --stacktrace ./mixql-docs/antora-playbook-local.yml
    ```
   3.2. Git repos
   - Generate playbook from git repos via antora-playbook.yml
   ```
   docker run -v $PWD:/antora --rm -t local/antora:lunr --stacktrace ./mixql-docs/antora-playbook.yml
   ```  
4. Run ./mixql/mixql-docs/public/index.html


