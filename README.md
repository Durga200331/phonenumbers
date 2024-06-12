import opencage
import phonenumbers
from myphone import number
from phonenumbers import geocoder

pepnumber=phonenumbers.parse(number)

location = geocoder.description_for_number(pepnumber,"en")
print(location)


from phonenumbers import carrier
service_pro = phonenumbers.parse(number)
print(carrier.name_for_number(service_pro,"en"))

from opencage.geocoder import OpenCageGeocode
key = '1aba5276a044427281f44331f2f21161'

sannumber = phonenumbers.parse(number)

yourlocation = geocoder.description_for_number(sannumber,"en")
print(yourlocation)

from opencage.geocoder import OpenCageGeocode

geocoder = OpenCageGeocode(key)

query = str(yourlocation)

results= geocoder.geocode(query)
##print(results)
lat = results[0]['geometry']['lat']

lng = results[0]['geometry']['lng']

print(lat,lng)



##
