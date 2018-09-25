# serverless-certificate-creator

this serverless plugin creates certificates that you need for your custom domains in API Gateway.

# Usage

        npm i serverless-certificate-creator --save

open serverless.yml and add the following:

        plugins:
        - serverless-certificate-creator

        custom:
        customCertificate:
            certificateName: 'abc.somedomain.io' //required
            idempotencyToken: 'abcsomedomainio' //optional
            hostedZoneId: 'XXXXXXXXX' //required
            region: eu-west-1 // optional - default is us-east-1 which is required for custom api gateway domains of Type Edge (default)


now you can run:

        serverless create-cert