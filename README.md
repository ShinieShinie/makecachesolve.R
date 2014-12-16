makecachesolve.R
================

create a cache of solv of a matrix ,and then create a function to learn it .
makeCacheMatrix<-function(x=numeric()){
  s<-NULL#the first Value
  set<-function(y){
    x<<-y
    s<<-NULL
  }
  get<-function()x
  setSolve()<-function(solve) s<<-solve# make a solve 
  getmsolve<-function() s
  list(set=set,get=get,set=setxolve,getsolve=getsolve)
}# create a cache of solve
cacheSolve<-function(x, ...){
  m<-x$getsolve()
  if(!is.null(s)){
    message("getting cached data")
    return(s)
  }
  data<-x$get()
  s<-solve(data,...)
  x$setsolve(s)
  s
}# try to find a cache
