# Zactor APIs: Finance
We've developed a suite of APIs tailored for use within the Mutual Fund industry. These APIs provide a comprehensive set of tools and functionalities to streamline processes, enhance efficiency, and enable seamless integration within the mutual fund ecosystem.

## PAN Check API

Use this API to check the PAN status and determine if the user needs to complete KYC again based on updated KYC regulations.

### Route
<baseUrl>/v1/zactor-apis/pan/check

### Request
Attributes | Description | Type
|---|---|---|
| pan | Pan Number, Eg. ABCDE1234F | String | 

### Response
Attributes | Description | Type
|---|---|---|
| pan | Pan Number | String |
| holderName | KYC Holder Name | String |
| status | KYC Status | Boolean |
| reason | if status false, reason for it. Eg: Hold, Rejected, etc | String |
| doKycAgain | true means user is "KYC Validated". False means user is "KYC Registered" or "KYC ON-Hold" an KYC has to be done again | Boolean |
| kycCreationDate | KYC Creation Date | String |
| kycLastStatusUpdatedDate | KYC Status Last Updated Date | String |
| kycMode | Mode by which user has completed the KYC | String |
| addressProofPer | Indicates the Address proof submitted is Aadhaar or Non-Aadhaar based KYC for Permanent address| String |
| addressProofCor | Indicates the Address proof submitted is Aadhaar or Non-Aadhaar based KYC for correspondence address | String |
| detailsSource | KRA Source of KYC data  | String |


### Example Request
```
curl --location '<baseUrl>/v1/zactor-apis/pan/check' \
--header 'token: <authToken>' \
--header 'Content-Type: application/json' \
--data '{
    "pan": "abcde1234f"
}'
```


### Example Response
```
{
  pan: 'ABCDE1234F',
  holderName: 'Tony Stark',
  status: true,
  reason: "",    
  doKycAgain: false,
  kycCreationDate: '30-11-2021 11:51:38',
  kycLastStatusUpdatedDate: '',
  kycMode: 'Normal',
  addressProofPer: 'Aadhar Digilocker',
  addressProofCor: 'Aadhar Digilocker',
  detailsSource: 'CAMSKRA'
}
```

## APIs In Timeline

- Mutual Fund fact-sheet
- Detailed Mutual Fund Research
  

## Contact for Auth Keys

E-mail: contact@zactortech.com, shivam@zactortech.com

Mobile: +91-77175 48040

Company Linkedin: [Zactor Tech](https://www.linkedin.com/company/zactor-tech)

Developer Linkedin: [Shivam Parihar](https://www.linkedin.com/in/shivamparihar/)
