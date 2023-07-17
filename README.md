Android E-Commerce app - PayTM Gateway
===================
Android simple e-commerce with PayTM payment gateway integrated.


Changing the REST endpoint
===================
Currenlty this repo uses the demo REST API provided. You can build the backend project and change the base url in **app/build.gradle** file.
```gradle
productFlavors {
        dev {
            buildConfigField "String", "BASE_URL", "\"https://demo.androidhive.info/paytm/public/api/\""
            buildConfigField "String", "PAYTM_CALLBACK_URL", "\"https://securegw-stage.paytm.in/theia/paytmCallback?ORDER_ID=%s\""
            buildConfigField "boolean", "IS_PATM_STAGIN", "true"
        }

        prod {
            buildConfigField "String", "BASE_URL", "\"https://demo.androidhive.info/paytm/public/api/\""
            buildConfigField "String", "PAYTM_CALLBACK_URL", "\"https://securegw.paytm.in/theia/paytmCallback?ORDER_ID=%s\""
            buildConfigField "boolean", "IS_PATM_STAGIN", "false"
        }
    }
```
