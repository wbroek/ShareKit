# Sharekit Overhaul 

*Wouter van den Broek*<br />
*woutervdbroek@gmail.com*<br />

Includes: Sharekit by Nate Weiner (http://getsharekit.com)

## What is it

Sharekit is a content sharing framework developed by Nate Weiner and used by many IOS developers. Unfortunately Sharekit hasn't been updated for a long time, last update was 23th of november 2010.<br />
This overhaul version has as goal to have all the libraries used by the share services up to date and implement some new ones; also to add some more languages to Sharekit and fix the most annoying bugs 

## Big changes

These changes are changes which need code modification in your code

### Facebook
Added native Facebook support which works in iOS 6<br>
If the device runs on iOS 5 Facebook connect is used, see below

### Facebook connect

Facebook connect has changed the way they authenticate the user on the iphone. In the previous release of Sharekit it was done in a browser view where the user needed to enter his email and password.<br />
Now Facebook connect looks if you have the Facebook app installed on your iPhone it get's the credentials from the app. If the Facebook app is not installed it will launch safari where the user needs to enter there email and password and it he is authenticated Facebook will call the URL scheme of your app.<br />
#### How to integrate Facebook connect with Sharekit in your app
Enter the AppID in SHConfig<br />
Add an URL scheme to your apps plist with the value FB$AppID (look for an example in the ShareKit-Info.plist)<br />
In your AppDelegate add the delegate functions (BOOL)application:(UIApplication *)application handleOpenURL:(NSURL *)url and (BOOL)application:(UIApplication *)application openURL:(NSURL *)url sourceApplication:(NSString *)sourceApplication annotation:(id)annotation to handle the URL scheme (look in de example in ShareKitAppDelegate)


### Twitter
Added native support for Twitter which is intergrated in IOS 5.<br />
If there is an account present it will use the native functions, if not it will use the normal procedure.

### Delicious

Delicious has been removed! 
Yahoo sold Delicious and there API is not matured yet. Will be added later when the API is solid.

## Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
