# Build documentation for mixql.org

## Quick build

1. You have [Docker](https://docs.docker.com/desktop/) installed 
   1. Build local Antora builder image
    ```
    docker build -t local/antora:lunr -f ./mixql-docs/Dockerfile.lunr .
    ```

2. Local build
   1. Download all needed mixql-* repo into ./mixql. Site will be generated in the mixql-docs/public folder.
    ```
    mkdir mixql && mixql
    git clone https://github.com/mixql/mixql-test-env.git
    git clone https://github.com/mixql/mixql-platform.git
    git clone https://github.com/mixql/mixql-core.git
    ```
   2. Generate site via local playbook.yml

    ```
   /mixql$ docker run -v $PWD:/antora --rm -t local/antora:lunr --extension @antora/lunr-extension  --stacktrace ./mixql-docs/antora-playbook-local.yml
    ```
3. Build from git
    1. Download mixql-docs repo into ./mixql. Site will be generated in the mixql-docs/public folder.
    ```
    mkdir mixql && mixql
    git clone https://github.com/mixql/mixql-test-env.git
    git clone https://github.com/mixql/mixql-platform.git
    git clone https://github.com/mixql/mixql-core.git
    ```
4. Generate playbook from git repos

```
docker run -v $PWD:/antora --rm -t local/antora:lunr --stacktrace ./mixql-docs/antora-playbook.yml
```  
5. Run mixql-docs/public/index.html

## Links

### Antora
- https://antora.zulipchat.com/ Antora chat
- https://docs.antora.org/antora/latest/how-antora-works/ Antora Docs
- https://github.com/owncloud/docs Antora best practice from Owncloud
- https://redhat-documentation.github.io/modular-docs/#introduction_{context} Redhat modular doc
- https://docs.magnolia-cms.com/product-docs/6.2/contribute/index.html Example: How to contribute
- https://antora.zulipchat.com/#narrow/stream/282405-tips-.F0.9F.92.A1/topic/playbook.20branch/near/301914551 Playbook in branch

### Antora Deploy
- https://gitlab.com/antora/docker-antora Docker Antora

### Asciidoc
- https://docs.asciidoctor.org/ 
- https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/ 

## Search engine (Antora Lunr extension)
- https://lunrjs.com/guides/searching.html
- https://gitlab.com/antora/antora-lunr-extension

## Examples
- https://github.com/asciidoctor/asciidoc-docs
- https://github.com/asciidoctor/asciidoctor-intellij-plugin/tree/main/doc
- https://docs.mulesoft.com/general/
- https://github.com/apache/felix-antora-site
- https://github.com/apache/isis-antora
- https://github.com/couchbaselabs/tutorials-contrib 
- https://github.com/Deep-Symmetry/beat-link-trigger/tree/guide-7.0/doc
- https://datahandwerk.gitlab.io/dhw/index.html
- https://github.com/apache/solr/tree/main/solr/solr-ref-guide
- https://github.com/apache/solr/blob/main/dev-docs/ref-guide/antora.adoc
- https://docs.magnolia-cms.com/welcome/index.html 
- https://github.com/spring-projects/spring-security/tree/docs-build

## Complex projects
### Asciidoctor
- https://github.com/asciidoctor/docs.asciidoctor.org Playbook Antora
- https://github.com/asciidoctor/asciidoctor-docs-ui

### SOLR
- https://github.com/apache/solr/blob/main/solr/solr-ref-guide/playbook.template.yml 
- https://github.com/apache/solr
- https://github.com/apache/solr/tree/main/dev-docs

### Owncloud
- https://github.com/owncloud/docs/blob/master/antora.yml
- https://github.com/owncloud/docs-ui UI
- 

### Camel
- https://github.com/apache/camel/blob/main/docs/antora-playbook-local-xref-check.yml

### Other
- https://github.com/owncloud/docs-ui/blob/master/.github/settings.yml

## UI examples
- https://docs.antora.org/antora-ui-default/ Antora UI
- https://gitlab.com/antora/antora-ui-default
- https://github.com/asciidoctor/asciidoctor-docs-ui 
- https://github.com/apache/felix-antora-ui 
- https://github.com/apache/solr/tree/main/solr/solr-ref-guide 


