# Sharekit Overhaul 

*Wouter van den Broek*<br />
*woutervdbroek@gmail.com*<br />

Includes: Sharekit by Nate Weiner (http://getsharekit.com)

## What is it

Sharekit is a content sharing framework developed by Nate Weiner and used by many IOS developers. Unfortunately Sharekit hasn't been updated for a long time, last update was 23th of november 2010.
This overhaul version has as goal to have all the libraries used by the share services up to date and implement some new ones; also to add some more languages to Sharekit and fix the most annoying bugs 

## Big changes

These changes are changes which need code modification in your code

### Facebook connect

Facebook connect has changed the way they authenticate the user on the iphone. In the previous release of Sharekit it was done in a browser view where the user needed to enter his email and password.
Now Facebook connect looks if you have the Facebook app installed on your iPhone it get's the credentials from the app. If the Facebook app is not installed it will launch safari where the user needs to enter there email and password and it he is authenticated Facebook will call the URL scheme of your app.
Your app needs to have an URL scheme that Facebook connects generates; normally fb<APP_ID>. URL schemes are defined in the application plist. It also needs the function (BOOL)application:(UIApplication *)application handleOpenURL:(NSURL *)url in your application delegate. Look at the example app for the code.



## Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.