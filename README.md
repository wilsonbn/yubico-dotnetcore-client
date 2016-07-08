# yubico-dotnetcore-client
dotnetcore port for Yubico validation protocol 2.0 client https://developers.yubico.com/yubico-dotnet-client/

To use this with YubiCloud you will need a free clientId and apiKey from https://upgrade.yubico.com/getapikey

For more details on how to use YubiKey OTP libraries, visit https://developers.yubico.com/OTP[developers.yubico.com/OTP].

=== Usage ===

[source, csharp]
----
YubicoClient client = new YubicoClient(clientId, apiKey);
IYubicoResponse response = client.Verify(otp);
if(response.Status == YubicoResponseStatus.Ok) 
{
  // validation success
} 
else 
{
  // validation failure
}
----
