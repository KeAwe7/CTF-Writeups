# Challenge

## Description

My friend swears he saw a Russian plane in the US this June, but I don't believe him. He also says he saw it was parked next to a plane owned by an infamous former president!

Can you find the registration number of this Russian plane, the FAA airport code of where the plane was spotted parked next to the other, as well as the registration number of the plane owned by that president?

My friend also tells me that a few days earlier, ANOTHER Russian plane flew to the US. Find the city that Russian plane was closest to at 21:07:40 Z during its flight to the US!

Flag format: csawctf{RegistrationNumberRUS_AirportCode_RegistrationNumberUS_CityName}

Do not include any special characters (dashes, etc)

## My Solution

Based on the description we're gonna need information about THREE planes, two Russian planes and an American one. I scoured the internet for Russian planes flying to US in June and found this information:


```
Russian-built Ilyushin Il-96-300, belonging to the Russian government’s fleet, flew from Moscow (VKO) to New York (JFK). The plane, which has the registration code RA-96019, is roughly 15 years old, and operated with the flight number RSD738.
```

I also saw a Twitter post about a parked Russian plane next to a former US president plane, the post also included a lot of information including the airport, the owner of the plane, and the registration code of the plane:

```
- Registration code (Russian Plane) = RA-96018
- FAA airport code of where it was spotted = IAD - Dulles International Airport
- Infamous former president = Trump
- Registration code (Trump's Plane) = N757AF
```

The first information we found turned out to be the other Russian plane that flew to the US.
Searching for flight path of RSD738, I found this:

```
City name = https://data.dictatoralert.org/flight/2660664/ -> Trenton
```

I now have these information:

1. RegistrationNumberRUS = **RA-96019** or **RA-96018**
2. FAA Airport Code = **IAD**
3. RegistrationNumberUS = **N757AF**
4. CityName = **Trenton**

By guessing which Russian registration number to use, I got the flag:

## Flag

<details> 
  <summary>Flag</summary>
   csawctf{RA96018_IAD_N757AF_Trenton}
</details>


Not gonna lie, this took me a long time to solve. I spent most of my time trying to figure out the CityName (before I found that website above), I tried every single city that the plane flew over starting from Reykjavik, Iceland. I think in total it took me 2-3 hours.