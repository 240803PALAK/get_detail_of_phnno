# get_detail_of_phnno
Get detail of Phone Number like Timezone , Carrier, Register.


import phonenumbers
from phonenumbers import timezone,geocoder,carrier
number=input("Enter your no. with (+_ _): ")
phone=phonenumbers.parse(number)
time=timezone.time_zones_for_number(phone)
car=carrier.name_for_number(phone,"en")
reg=geocoder.description_for_number(phone,"en")
print(phone)
print(f"Time Zone: {time}")
print(f"Carrier: {car}")
print(f"Registration: {reg}")
