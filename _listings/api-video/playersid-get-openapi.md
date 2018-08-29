---
swagger: "2.0"
x-collection-name: api.video
x-complete: 0
info:
  title: API.Video Get Players
  description: Get players.
  version: 1.0.0
host: ws.api.video
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /videos/{id}/thumbnail:
    parameters:
      summary: Parameters Videos Thumbnail
      description: Parameters videos thumbnail.
      operationId: parametersVeosThumbnail
      x-api-path-slug: videosidthumbnail-parameters
      responses:
        200:
          description: Successful response
      tags:
      - Parameters
      - Videos
      - Thumbnail
    patch:
      summary: Patch Videos Thumbnail
      description: |-
        Pick a thumbnail from the given time code.

        It may take up to 1h before the new thumbnail to be delivered by our CDN.
      operationId: patchVeosThumbnail
      x-api-path-slug: videosidthumbnail-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Videos
      - Thumbnail
    post:
      summary: Post Videos Thumbnail
      description: It may take up to 1h before the new thumbnail to be delivered by
        our CDN.
      operationId: postVeosThumbnail
      x-api-path-slug: videosidthumbnail-post
      responses:
        200:
          description: Successful response
      tags:
      - Videos
      - Thumbnail
  /videos/{videoId}:
    parameters:
      summary: Parameters Videos Videoid
      description: Parameters videos videoid.
      operationId: parametersVeosVeo
      x-api-path-slug: videosvideoid-parameters
      responses:
        200:
          description: Successful response
      tags:
      - Parameters
      - Videos
    patch:
      summary: Patch Videos Videoid
      description: Patch videos videoid.
      operationId: patchVeosVeo
      x-api-path-slug: videosvideoid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Videos
  /players/{id}:
    parameters:
      summary: Parameters Players
      description: Parameters players.
      operationId: parametersPlayers
      x-api-path-slug: playersid-parameters
      responses:
        200:
          description: Successful response
      tags:
      - Parameters
      - Players
    patch:
      summary: Patch Players
      description: It may take up to 10min before the new player configuration is
        available from our CDN.
      operationId: patchPlayers
      x-api-path-slug: playersid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Players
    get:
      summary: Get Players
      description: Get players.
      operationId: getPlayers
      x-api-path-slug: playersid-get
      responses:
        200:
          description: Successful response
      tags:
      - Players
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---