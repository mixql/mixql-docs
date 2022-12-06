# mixql_docs

## Main Links

### Antora 
- https://github.com/ntlegion/mixql_docs  This repo
- https://antora.zulipchat.com/ Antora chat
- https://docs.antora.org/antora/latest/how-antora-works/ Antora Docs
- https://github.com/owncloud/docs Antora best practice from Owncloud
- https://redhat-documentation.github.io/modular-docs/#introduction_{context} Redhat modular doc
- https://docs.magnolia-cms.com/product-docs/6.2/contribute/index.html Example: How to contribute 
- https://antora.zulipchat.com/#narrow/stream/282405-tips-.F0.9F.92.A1/topic/playbook.20branch/near/301914551 Playbook in branch

### Antora Deploy    
- https://gitlab.com/antora/docker-antora Docker Antora

#### Quick test

    rm -rf ./build/* 
    docker run -v $PWD:/antora --rm -t antora/antora --stacktrace antora-playbook.yml
    touch build/site/.nojekyll
    
    # generate with index
    docker build -t local/antora:lunr -f Dockerfile.lunr .
    docker run -v $PWD:/antora --rm -t local/antora:lunr --extension @antora/lunr-extension  --stacktrace antora-playbook.yml
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


#### SOLR
- https://github.com/apache/solr/blob/main/solr/solr-ref-guide/playbook.template.yml 
- https://github.com/apache/solr
- https://github.com/apache/solr/tree/main/dev-docs

#### Owncloud
- https://github.com/owncloud/docs/blob/master/antora.yml
- https://github.com/owncloud/docs-ui UI
- 

### Camel
- https://github.com/apache/camel/blob/main/docs/antora-playbook-local-xref-check.yml
### Other
- https://github.com/owncloud/docs-ui/blob/master/.github/settings.yml

### UI examples
- https://docs.antora.org/antora-ui-default/ Antora UI
- https://gitlab.com/antora/antora-ui-default
- https://github.com/asciidoctor/asciidoctor-docs-ui 
- https://github.com/apache/felix-antora-ui 
- https://github.com/apache/solr/tree/main/solr/solr-ref-guide 


