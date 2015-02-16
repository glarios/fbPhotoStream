<h1>fbPhotoStream</h1>
<p>fbPhotoStream is a simple, light-weight jQuery plugin that allows you to display Facebook photos from a <strong><a href="https://www.facebook.com/help/215496745135618" target="_blank">public</a></strong> album. Just set the album id, and the rest is optional.</p>
<p>It has a a few design options like grid, collage, or circle mode, but you can customize the look to match your needs by adding your own CSS. You can pass several formatting options including width, height, etc., as well as setting whether you want to show captions or link back to Facebook.</p>
<p>All you need to do is include the plugin file into your webpage, create a target wrapper element, and pass that element's id into the method.</p>
<h2>Demo</h2>
<a href="http://www.gerardolarios.com/facebook-photo-stream/" target="_blank">View demo.</a>
<h2>Required Files</h2>
<ol>
  <li><a href="http://www.jquery.com/" target="_blank">jQuery Core JavaScript Library</a></li>
  <li><a href="http://www.gerardolarios.com/facebook-photo-stream/js/facebook-photo-stream.min.js" target="_blank">facebook-photo-stream.min.js</a></li>
</ol>
<p>Include the above files into your webpage and invoke the <code>fbPhotoStream()</code> method.</p>
<p>Remember, you can add your own CSS to style the results to match your needs in "raw" display mode.</p>

<h2 id="how-to-use">How to Use</h2>
<ol>
  <li>First, make sure that your Facebook photo album is public. You can change the privacy settings by following <a href="https://www.facebook.com/help/215496745135618" target="_blank">this documentation</a>.</li>
  <li>Next, you need to get the album id. You can get this by clicking on the album in Facebook, then from the URL copy the number that is between the "photos/a." and the next "." (highlighted in blue in the image below).<br><img src="https://github.com/glarios/fbPhotoStream/blob/master/fburl.jpg" /></li>
  <li>Create an empty wrapper element, in this case a <code>&lt;div&gt;</code>, and assign a unique id or class to it. Then pass that id into the fbPhotoStream() method along with the album id.</li>
</ol>

<pre><code><div id="fbPhotoStream"></div>
<script type="text/javascript">		
$(document).ready(function(){ 
    $('#fbPhotoStream').fbPhotoStream(); 
});
</script></code></pre>

<h2>Configuration</h2>
<p> fbPhotoStream is pretty much ready to go, and the only necessary parameter to get started is the <code>album id</code>. There are several additional options that you can use to match your needs. Pass these options as an object into the <code>fbPhotoStream()</code> method like this:</p>

<pre><code>$('#fbPhotoStream').fbPhotoStream({ 
    album:'10152554461003426',
    count:5,
    format:'ul'
});</code></pre>

<h2>Options</h2>
| Property      | Type          | Default  | Description |
| ------------- |:-------------:| -------- | ----------- |
|album|string|<strong>No default, must be set as option.</strong>|The id of the Facebook photo album. See how to get that <a href="#how-to-use">here</a>.|
            |display|string|grid|Preset display formats. Options include 'grid','collage', or 'circle'.|
			|displayWidth|string|200px|Width of the images used in one of the display presets.|
			|displayHeight|string|200px|Height of the images used in one of the display presets.|
			|count|integer|25 (maximum allowed by Facebook).|The number of photos to display. Facebook puts a limit of 25.|
            |linked|boolean|true|Whether or not the image links back to itself in Facebook.|
            |theClass|string|No default.|Allows for classes to be assigned to the elements created. If adding multiple, separate by spaces like such:<br><code>theClass:'row feature pull-left'</code>.|
            |format (used only with display:'raw')|string|ul|The format in which the results are displayed. Options are 'ul','div', or 'none'. Using 'none' outputs the image tag in an anchor, or just the image tag by itself (depending on whether 'linked' is set to false).|
			|size (used only with display:'raw')|string|medium|The size of the images returned by Facebook. Options are 'large','medium', or 'small'.|
			|caption (used only with display:'raw')|boolean|false|Whether to include the image caption or not.|

        
<h2>License</h2>

<p>fbPhotoStream is free to use under the <a href="http://jquery.org/license" target="_blank">MIT/GPL</a> license for any application.</p>
<h2>Author</h2>
<p>This plugin was written by <a href="http://www.gerardolarios.com" target="_blank">Gerardo Larios</a>.</p>
