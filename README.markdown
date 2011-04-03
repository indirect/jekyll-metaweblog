## jekyll-metaweblog

A stand-alone server that will expose a Jekyll source folder via the Blogger / MT / Wordpress XML-RPC metaweblog interface, allowing you to create/edit/delete posts and pages using a GUI client, such as Marsedit.



### Usage

  ruby server.rb --port 4040 --root /path/to/jekyll/folder

Then point your weblog client to http://localhost:4040/ and start editing.



### Limitations

If you change the slug, date, or the text filter of an entry, you'll need to refresh the blog after you save it. (I use the filename as the post ID, but changing the slug or the filter changes the filename, so the GUI tool will lose the connection). I might be able to work round this.

Not all clients work. Let me know if you're using a weird client and having problems. And by weird, I mean, not Marsedit or Ecto, which are the two I have here.



### TODO

* username/password support, so it's safe to run on a remote server.

* run the jekyll processor in the same process, so you can run a single command line that will build your blog _and_ expose it to GUI clients.

* file upload support.

* Support for more clients (this mostly consists of trying them and fixing the broken things)

* category support (assuming jekyll does categories and anyone cares)

* Support for wordpress IOS clients. This is _hard_, because they're using undocumented API calls and make assumptions about what IDs look like that I'm not happy with (it assumes they're numbers).

* everything else in the code with "TODO" by it.

* fix all the bugs. AHAHAHAHAHAHAHAH
