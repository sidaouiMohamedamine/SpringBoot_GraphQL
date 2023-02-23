# SpringBoot_GraphQL
/**********If you want to save an author but without books******************************/
mutation{
  saveAuthor(author:{id:5,name:"sidaoui"}){
    id
  	name
  }
}
/**********If you want to retreive all authors******************************/
query{
getAuthor{
id
name
books {
id
title
description
pages
}
}
}
/**********If you want to retreive an author by id******************************/
query{
getAuthorById(id:1){
id
name
books {
id
title
description
pages
}
}
}
/********If you want to add a new book******************************/
mutation{
  saveBook(book:{title:"REST API tutorial",description:"Tutorial",pages:300,id:2})
{
  id  
}
}
/********If you want to retreive all books******************************/
query{
  getAllBooks{
     title
      description
    	pages
    author{
      id
      name
    }
        
  }
    }
  
