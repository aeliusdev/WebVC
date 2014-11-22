WebVC
=====

A JavaScript class for checking browser &amp; mobile compatibility.

<h2>Features</h2>

<ul>
  <li>Browser Info</li>
  <li>Detect the current browser name. For example Chrome.</li>
  <li>Detect the current browser version to no decimal places. For example Chrome 10.</li>
  <li>Detect the current latest browser version. For example Chrome 10.0.167.</li>
  <li>Detect the current application name. For example Netscape.</li>
  <li>Detect current orientation of the browser window.</li>
</ul>

<ul>
  <li>Mobile Detection</li>
  <li>Detect whether the current browser is a mobile browser.</li>
  <li>Detect a change in orientation and provide a callback function. For example when some one rotates their iPhone into portrait view you can create a callback telling them to rotate into landscape.</li>
</ul>

<h2>Usage</h2>

<h3>Browser Information</h3>

The <code>WebVC.browser();</code> method allows you get current browser information.

<ul>
  <li>Browser Name: <code>WebVC.browser().name</code></li>
  <li>Browser Major Version: <code>WebVC.browser().version</code></li>
  <li>Browser Current Version: <code>WebVC.browser().version_accurate</code></li>
  <li>Browser Application Name: <code>WebVC.browser().app_name</code></li>
</ul>

<h3>Detecting a Mobile Browser</h3>

Use <code>WebVC.is_mobile()</code> to detect mobile browsers.

<pre>
if ( WebVC.is_mobile() ) 
{
  
  alert( "Mobile Browser Present!" );

}
</pre>

<h3>Detecting Orientation</h3>

Use <code>WebVC.orientation()</code> to detect the current orientation.

<pre>alert( WebVC.orientation() );</pre>

<h3>Detecting Mobile Orientation & Changes in Orientation</h3>

Use <code>WebVC.mobile_orientation()</code> to detect the current orientation.

<pre>alert( WebVC.mobile_orientation() );</pre>

Use <code>WebVC.mobile_orientation_change( function_name )</code> to detect a change in orientation.

Parameters: function_name - The name of the callback function when a change of orientation has been detected.

<pre>

function alertCurrentOrientation () 
{
  
  alert( WebVC.mobile_orientation() );

}

WebVC.mobile_orientation_change( alertCurrentOrientation );

</pre>

Thanks for reading!
