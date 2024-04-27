# Zactor APIs: Finance
We have creating a collection a APIs that can be used for Mutual Fund industry

## PAN Check API

Use this API to get the PAN status.

### Route
<baseUrl>/v1/zactor-apis/pan/check

### Request
Attributes | Description | Type
|---|---|---|
| pan | Pan Number, Eg. ABCDE1234F | String | 

### Response
Attributes | Description | Type
|---|---|---|
| pan | pan | String | 
| holderName | holderName | String |
| status | status | String |
| kycCreationDate | kycCreationDate | String |
| kycLastStatusUpdatedDate | kycLastStatusUpdatedDate | String |
| modificationDate | modificationDate | String |
| statusOfModification | statusOfModification | String |
| missingFields | missingFields | String |
| holdOrDeactiveRemark | holdOrDeactiveRemark | String |
| kycMode | kycMode | String |
| inPersonVerification | inPersonVerification | String |
| addressProofPer | addressProofPer | String |
| addressProofCor | addressProofCor | String |
| detailsSource | detailsSource | String |


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
  doKycAgain: true,
  kycCreationDate: '30-11-2021 11:51:38',
  kycLastStatusUpdatedDate: '',
  modificationDate: '',
  statusOfModification: '005',
  missingFields: '',
  holdOrDeactiveRemark: '',
  kycMode: 'Normal',
  inPersonVerification: 'E',
  addressProofPer: 'Aadhar Digilocker',
  addressProofCor: 'Aadhar Digilocker',
  detailsSource: 'CVLKRA'
}
```

## Contact for Auth Keys

E-mail: shivam@zactortech.com, contact@zactortech.com

Mobile: +91-77175 48040

Company Linkedin: [Zactor Tech](https://www.linkedin.com/company/zactor-tech)

Personal Linkedin: [Shivam Parihar](https://www.linkedin.com/in/shivamparihar/)
