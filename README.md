# MpesaDaraja.Net
NugetPackage for .Net

Install the Nuget Package by going to Package Console Manager and type
Install-Package MPESADARAJA -Version 1.0.4

For C2B 
include namespace
using MpesaDaraja;
Then call the async Method  
MpesaC2B.InititateCheckout(int paybill, int amount, string phone, int reference, string consumerkey, string consumersSecret, string confirmationUrl, string validationUrl, bool IsSandBox)

For Examples To Use It;

  public  async static Task<string> InitiateC2B(int paybill, int amount, string phone, int reference, string consumerkey, string consumersSecret, string confirmationUrl, string validationUrl, bool IsSandBox)
        {
           
            string message = await MpesaC2B.InititateCheckout(paybill, amount, phone, reference, consumerkey, consumersSecret, confirmationUrl, validationUrl, IsSandBox);
            return message;
        }
        
        
        
        
        For Authentication Call The Method;
         Authentication.AuthKey(string consumerkey, string consumersSecret,bool IsSandBox);
