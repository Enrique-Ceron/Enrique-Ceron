- nombre : Actualizar ID de README 
  : github -contentful-readme 
  uses : Merlin04/github-contentful-readme@v[Insertar la última versión aquí, ver https://github.com/Merlin04/github-contentful-readme/releases] 
  env :
     GITHUB_TOKEN : ${{ secrets.GITHUB_TOKEN }} 
  con :
     headerKey : " github-header "
     subheaderKey : " github-subheader "
     footerKey : " github-footer "
     setOfProjectsCollectionId : " proyectos-colección-id"
     urlKey : " website-url "
     projectsLimit : 4 
    contentfulAccessToken : ${{ secrets.CONTENTFUL_ACCESS_TOKEN }} 
    contentfulSpaceId : ${{ secrets.CONTENTFUL_SPACE_ID }}``` 
- Es posible que desee programar esto para que se ejecute cada 10 minutos, péguelo debajo `en` :
 ` ` ` programación yaml 
: 
  - cron: "*/10 * * * *"
