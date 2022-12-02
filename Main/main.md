import phonenumbers
import urllib.request


from myphone import number

from phonenumbers import geocoder

key = '901d715281de4bb1a399b0dd63121606'

pepnumber = phonenumbers.parse(number)

location = geocoder.description_for_number(pepnumber , "en")

print(location)

from phonenumbers import carrier

service_pro = phonenumbers.parse(number)

print(carrier.name_for_number(service_pro , "en"))


from opencage.geocoder import OpenCageGeocode

geocoder = OpenCageGeocode(key)

query = str(location)

results = geocoder.geocode(query)

print(results.encode("utf-8"))
