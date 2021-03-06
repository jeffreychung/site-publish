Site Publish for App Engine
===========================

Site Publish is a simple file-based content publishing system that runs on
Google App Engine.  It is designed to be a part of a dynamic website that also
hosts static content.

This is a basic implementation that demonstrates the
start-upload-commit design pattern described in the talk.  There is
plenty of room for improvement and extension.  And possibly a few
bugs.  Enjoy!

To demonstrate publishing on a development server, start the server:

    dev_appserver.py app
  
Then publish the included demo content:

    ./sp publish content/*

To use the client with a deployed app, generate a new discovery
document with the app's hostname:

    cd app
    ~/google_appengine/endpointscfg.py gen_discovery_doc -o ../tool -f rest --hostname=site-publish.appspot.com services.SitePublishApi

To use the API Explorer with your deployed app, you must be signed in to your site with your app administrator account.  To sign in, visit this URL, then sign in with the Google account you use to deploy the app:

    https://YOUR-APP-ID.appspot.com/_sitepublish/

Then visit the link shown to the API Explorer.


## License

Copyright 2013 Google Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
