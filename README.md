# About DevSecOps
Development &amp; Security &amp; Operations all in one

# Development

## Concept
###Data Structre
###Algorithm
###Program Design Evolution
#### MVC-> DDD -> OOP -> Design Pattern/Anti Design Pattern  
###System Design
#### 
 
## FrontEnd

## BackEnd 

## Unit Testing

## E2E (end to end Testing) 


# Security
## Secret-Detection(Gitleaks)
## SAST(Sonarqbue)
## DAST(OWASP ZAP)
### web 
### funzzing

## SCA(3rd Party Dependency-Check + Sonarqbue License Check)
## Terrascan


# Operations
## CI flow

## CD flow
### Provision - Atlantis
#### plan
#### apply 
### Release - GitOps(ArgoCD)


# auto build-up and  genertate static web data (html + css + javascript)
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build

# build up your website 
docker run  -p 1988:80 -v ${PWD}/site:/usr/share/nginx/html:ro nginx:latest

# how to auto deploy to github pages
docker run --rm -it -v ~/.ssh:/root/.ssh -v ${PWD}:/docs squidfunk/mkdocs-material gh-deploy 


# mkdocs document
https://www.mkdocs.org/user-guide/writing-your-docs/

# more material for mkdocs
https://squidfunk.github.io/mkdocs-material/creating-your-site/



