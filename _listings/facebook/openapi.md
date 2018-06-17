---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 1
info:
  title: Facebook
  description: connect-to-the-social-network-with-the-graph-api-
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{application}/albums:
    get:
      summary: Get Application Albums
      description: The photo albums this application has created.
      operationId: getApplicationAlbums
      x-api-path-slug: applicationalbums-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Albums
  /{page}/albums:
    get:
      summary: Get Page Albums
      description: The photo albums this Page has uploaded
      operationId: getPageAlbums
      x-api-path-slug: pagealbums-get
      parameters:
      - in: path
        name: page
        description: Represents the ID of the page object
      responses:
        200:
          description: OK
      tags:
      - Page
      - Albums
  /{user}/albums:
    get:
      summary: Get User Albums
      description: The photo albums this user has created
      operationId: getUserAlbums
      x-api-path-slug: useralbums-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Albums
    post:
      summary: Post User Albums
      description: Creates an album for the user
      operationId: postUserAlbums
      x-api-path-slug: useralbums-post
      parameters:
      - in: query
        name: message
        description: Album description
      - in: query
        name: name
        description: Album name
      - in: query
        name: privacy
        description: Privacy settings for the Album
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Albums
---