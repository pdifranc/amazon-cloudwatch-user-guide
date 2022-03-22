# Configuring the CloudWatch RUM web client with CDN installation<a name="CloudWatch-RUM-configure-client"></a>

Your applications can use the code snippet generated by CloudWatch RUM to install the CloudWatch RUM web client from a content delivery network \(CDN\)\. The code snippet sits in the `<head>` tag of an HTML file and installs the web client by downloading the web client from a CDN, and then configuring the web client for the application it is monitoring\. The snippet is a self\-executing function which looks similar to the following\. In this example, the body of the snippet's function has been omitted for readability\.

```
<script>
(function(n,i,v,r,s,c,u,x,z){...})(
'cwr',
'00000000-0000-0000-0000-000000000000',
'1.0.0',
'us-west-2',
'https://client.rum.us-east-1.amazonaws.com/1.0.2/cwr.js',
{ /* Configuration Options Here */ }
);
<script>
```

## Arguments<a name="CloudWatch-RUM-configure-client-arguments"></a>

The code snippet accepts six arguments:
+ A namespace for running commands on the web client, such as `'cwr'`
+ The ID of the app monitor, such as `'00000000-0000-0000-0000-000000000000'`
+ The application version, such as `'1.0.0'`
+ The AWS Region of the app monitor, such as `'us-west-2'`
+ The URL of the web client, such as `'https://client.rum.us-east-1.amazonaws.com/1.0.2/cwr.js'`
+ Application\-specific configuration options\. For more information, see the following section\.

## Configuration options<a name="CloudWatch-RUM-configure-options"></a>

For information about the configuration options available for the CloudWatch RUM web client, see the [ CloudWatch RUM web client documentation](https://github.com/aws-observability/aws-rum-web/blob/main/docs/cdn_installation.md)