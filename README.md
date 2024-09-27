# bnm-df-wc

gcloud dataflow flex-template run "wordcount-date +%Y%m%d-%H%M%S"
--template-file-gcs-location "gs://bnm-wc/wordcount-flex-template-py.json"
--parameters input_file_pattern="gs://dataflow-samples/shakespeare/*"
--parameters output_file="gs://bnm-wc/output-"
--region "us-east4"
--subnetwork https://www.googleapis.com/compute/v1/projects/bnm-experimental/regions/us-east4/subnetworks/subnet-0
--disable-public-ips
