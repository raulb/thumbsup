# Thumbs Up

Thumbnails as a service or self-service (aka run it yourself). You give us
URL(s) and we'll return thumbnails. Pretty straight forward.

Thumbs Up can:

* Generate thumbnails of images
* Generate thumbnails of websites

## Generating Thumbnails

### Request

* HTTP Method: POST
* URL: https://www.thumbsup.io/thumbnail
* Body:

  ```js
  [
    {
      "url": "http://zeke.sikelianos.com/",
      "height": "300",
      "width": "400"
    },
    {
      "id": "unique_id",
      "foo": "bar",
      "url": "http://zeke.sikelianos.com/some-image.jpg",
      "height": "300",
      "width": "400"
    }
  ]
  ```

### Response

* Status: 200 OK
* Body:

  ```js
  [
    {
      "url": "http://zeke.sikelianos.com/",
      "height": "300",
      "width": "400"
      "thumbnail": "https://s3.aws.amazon.com/thumbsup/sha1.png"
    },
    {
      "id": "unique_id",
      "foo": "bar",
      "url": "http://zeke.sikelianos.com/some-image.jpg",
      "height": "300",
      "width": "400"
      "thumbnail": "https://s3.aws.amazon.com/thumbsup/sha1.png"
    }
  ]
  ```

## Todo

* Finish writing up API docs
* Draw the rest of the fucking owl
