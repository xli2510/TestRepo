import zipfile
import requests
import io

# Example: download dataset (replace with actual NOAA URL if provided)
url = "https://www1.ncdc.noaa.gov/pub/data/cdo/samples/PRECIP_HLY_sample_csv.csv.zip"
response = requests.get(url)

with zipfile.ZipFile(io.BytesIO(response.content)) as z:
    z.extractall("data/")
