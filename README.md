# Assignment-2---Coursera---R-Programming
makeCacheMatrix <- function(x = matrix()) {
  inverse_matrix <- NULL
  set <- function(y) {
    x <<- y
    inverse_matrix <<- NULL
  }
  get <- function() x
  setinverse <- function(inverse_matrix) inv <<- inverse_matrix
  getinverse <- function() inverse_matrix
  list(set=set, get=get, setinverse=setinverse, getinverse=getinverse)
}

cacheSolve <- function(x, ...) {
  inv <- x$getinverse()
  if(!is.null(inv)) {
    message("getting cached data.")
    return(inverse_matrix)
  }
  data <- x$get()
  inv <- solve(data)
  x$setinverse(inverse_matrix)
  inverse_matrix
}
