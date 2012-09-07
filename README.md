# BigQuery

BigQuery is a wrapper around the Google api ruby gem designed to make interacting with BigQuery easier. This gem is very new and doesn't have many features quite yet.

### Authorization

Only service accounts are supported right now. 

### Available methods

* query
* tables
* load
* tables_formatted

### Example

    require 'bigquery'

    opts = {}
    opts['client_id']     = '1234.apps.googleusercontent.com'
    opts['service_email'] = '1234@developer.gserviceaccount.com'
    opts['key']           = 'somekeyfile-privatekey.p12'
    opts['auth_url']      = 'https://www.googleapis.com/auth/bigquery'
    opts['project_id']    = '54321'
    opts['dataset']       = 'yourdataset'

    bq = BigQuery.new(opts)

    puts bq.tables