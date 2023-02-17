## PROBLEM
```
Figure out in which country each image was taken.
The first letter of every country's name will create the flag.
Countries with over 10 million inhabitants will have a capital letter.
Countries with less than one million inhabitants become an underscore.
```  
  &nbsp;  

## SOLUTION
We are provided with 17 images, each of a different country. We need to identify these countries, geoguessr-style, to construct a 17-character flag.
  &nbsp;  
Here I will present our solutions for each of the images, the specific techniques used to find each object and additional commentary. I will reveal the country the photos were taken in and if I have further information, the city or the exact coordinates. Several resources I used throughout include:
- Road Chevron Identification: https://www.geohints.com/Chevrons
- Bollard Identification: https://geohints.com/Bollards
- General Geoguessr Guide: https://somerandomstuff1.wordpress.com/2019/02/08/geoguessr-the-top-tips-tricks-and-techniques/
- More Geoguessr tips: https://geotips.net/
- Reverse Image Search: www.yandex.com

  &nbsp;  
### 1. Brazil (Rio de Janeiro | -22.9452929,-43.1633488)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/1.png"  width="500" height="300">

- Landmark: Christ the Redeemer statue on the top of the hill in the center

### 2. Russia (Moscow | 55.7534093,37.6210811)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/2.png"  width="500" height="300">

- Landmark: Red Square, Moscow

### 3. Estonia (Tallin | 59.4437727,24.7542789)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/3.png"  width="500" height="300">

- Text: The street sign reads "Kalamaja", which is a neighbourhood in Tallin, Estonia

  &nbsp;  

Fun Fact: The concrete structure in the center background is Tallinna Linnahall, an amphitheatre built for the 1980 Moscow Olympics. The glass building on the right is the Tallink spa and conference hotel, with a gian "Tallink" sign on the roof which was intentionally cut off in the photo. Would've been a dead giveaway.

### 4. Australia
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/4.png"  width="500" height="300">

- Bollard: White rectangular bollard with a horizontal red stripe is typical for Australia
- Landscape: red soil is characteristic for places like Australia and some parts of Africa (Kenya, Nigeria)

### 5. Kenya (Nairobi | -1.270328375102924, 36.85079769699517)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/5.png"  width="500" height="300">

- Language: The sign on the white and green building on the right is Swahili, a language spoken in the East coast of Africa
- Text: The Google Maps street name label is visible, and reads "Third St.", indicating this street is called Third Street.
- License Plates: Cars have yellow license plates, which is common across the EU and in Africa

  &nbsp;  

This one was tricky. Swahili would have been a dead giveaway, but we couldn't recognise it, mistook it for Arabic then started searching through all countries that speak Arabic. But we couldn't find a country that had a "Third St." road. It was **purely accidental** that we came across Kenya, because, while searching "Turkey Third St." in Google maps, we accidentally clicked on a suggestion for "Turkey Carpets: Third St., Nairobi, Kenya", and discovered it looked exactly the same as the image. A christmas Miracle!

### 6. Iceland ( Þjóðvegur | 65.3511738,-15.3966272)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/6.png"  width="500" height="300">

- Bollard: yellow bollard with a white tip is characteristic of Iceland
- Landscape: this sort of gray, flat, open and empty landscape is also quite characteristic of ICeland

  &nbsp;  

Fun fact: found the exact location by accident, just tried a bunch of random roads with a left bend in iceland. The mountains in the background are likely from Vatnajökull National Park.


### 7. Mongolia
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/7.png"  width="500" height="300">

- License Plate: The car has a white license plate with green lettering. It has 4 numbers followed by some letters. This is characteristic of Mongolian license plates.
- Architecture: The wooden fences, mongolian huts ("yurts") and low-rise, colourful housing is very specific to Mongolia



### 8. Eswatini (Mbabane | -26.2933309, 31.1265813)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/8.png"  width="500" height="300">

- Landscape: Smooth hills are unique to Eswatini and South Africa


In all honesty, We guessed this could be a country starting with E by meta-gaming it... so far, the letters spell "Break_m" so the next letter was likely to be either 'y' or a vowel.

### 9. Monaco (Port Hercule | 43.7371226, 7.4328427)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/9.png"  width="500" height="300">

- Landscape/ Meta Knowledge: The swimmer with the camera, tall buildings against a hilly backdrop and a dock full of yachts - Every half-decent geoguessr player can identify monaco from a mile away



### 10. Switzerland
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/10.png"  width="500" height="300">

- Flag: A swiss flag can be seen on the right side of the photo. A dead giveaway
- Landscape: Mountainous



### 11. Poland
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/11.png"  width="500" height="300">

- Bollard: White bollard with a slanted red stripe is only in poland
- Road Lines: Double white centre lines, no yellow lines - likely to be in Europe



### 12. Austria (Liezen | 47.56822557340595, 14.240171326822175)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/12.png"  width="500" height="300">

- Text: Road sign labelled "nikolaus-dumba-straße" points you to the Austrian municipality of Liezen
- Language: The use of the Eszett (letter 'ß' in the street sign) is exclusive to the German language
- Vehicle: Green public buses are used in certain areas of Austria

  &nbsp;  

The road sign should have been a dead giveaway but unfortunately, the image is so pixelated we kept reading dumba as "dumbo" and "nikolaus-dumbo-strasse" doesn't turn up anything in google maps unfortunately. We initially thought this could be Germany because of the language, but searching "germany nikolaus-" didn't turn up any potential close matches. Just as with the Kenyan Kristmas Miracle, we accidentally chanced across Austria while mindlessly scanning surrounding countries, and deciding to try "Austria nikolaus-" for fun since Austria is also German-speaking. The lesson here is a language is spoken in multiple countries, and it's worth trying all of them out in the search engine. Alternatively, hope for an Austrian Christmas Miracle.

### 13. Canada
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/13.png"  width="500" height="300">

- Road Lines: Center yellow line with white lines on the sides is common in the US/ Canada, not in Europe
- Power Lines: Similar to what you may find in some parts of Canada

  &nbsp;  

In truth, this was kind of a guess from the power lines and dropping in random Canadian roads in google maps street view. We found that the general landscape in the outskirts of Canadian towns looked very similar to the photo. So really, it was just a vibe.

### 14. Ecuador
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/14.png"  width="500" height="300">

- Chevron: Yellow and black chevrons, with the arrow being black, is only used in certain countries
- Vegetation: Tropical
- License Plate: Bright orange, on what looks to be a taxi. Ecuador uses orange license plates for their commercial vehicles.

  &nbsp;  

Using the chevron as a guide, we listed all countries that used the chevron design. Then, we narrowed this down to countries that were tropical. Finally, we investigated each option to see if they used orange license plates.

### 15. Bulgaria
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/15.png"  width="500" height="300">

- Architecture: Dilapidated
- Weather: Snow
- Landscape: gray
- ~~Hotel: trivago~~
- Streetview Date: On the bottom right of the image you can see the date it was taken by the Google Maps vehicle: March 2012
- Other observations: giant metal garbage collector, dirt path

  &nbsp;  

Using reverse image search, we ascertained that countries like Bulgaria and Serbia seemed to have similar landscape and architecture. We then went to Google Maps to investigate these countries. When looking at Bulgaria, we found that in its western remote areas, there were a lot of places that looked similar to the photo. On top of that, the latest Google Maps streetview images in these areas were taken in March 2012. The kicker? It was also snowing in those areas in March 2012. So Bulgaria wasn't a definite guess but it was a very strong, convincing possibility.

### 16. Albania (Elbasan | 40.7873086, 20.2856359)
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/16.png"  width="500" height="300">

- Chevron: White and black, with the arrow being white. Only used in certain countries.
- Landscape: Mountainous
- Meta: There is a crack in the sky (which I recently learned are called 'camera rifts') because the Google Maps team in the country didn't stitch the images together well. This is characteristic of Albania, Senegal and Montenegro.

  &nbsp;  

See, if I'd noticed the sky crack I would've solved this way faster. But unfortunately I attributed the sky crack to just a natural gap in the clouds... nature's buttcrack if you will. Instead, what we did was similar to #15: find countries that used the white and black chevron, narrowed it down to those with mountainous landscapes. Then, by now we already guessed the flag ended with "spacebar" so we guessed it was likely Albania. We corroborated this guess by exploring the mountainous areas in Albania, and managed to find roads that looked very similar to the photo.

### 17. Russia
<img src="https://github.com/adaisyx/idekCTF22-Writeup/blob/main/NMPZ/17.png"  width="500" height="300">

- Vegetation: The plant in the foreground is a Sakhalin plant, unique to Sakhalin (a Russian island) and Hokkaido

  &nbsp;  

I did in fact try to reverse image search the plant in the foreground, but when the I got a lot of Russian-related results, I assumed the reverse image search didn't work, since the answer to the 2nd image is Russia and I didn't think the countries would repeat. However, as I mentioned we'd already meta-gamed the answer, and had a strong inkling the last country began with R. So whether this image was of Rwanda, Russia or Romania didn't really matter, since all countries have a population >10million. Lesson learned - don't brush off your results. Also, meta-gaming is amazing.

  &nbsp;  

### SUMMARY
The flag is: **idek{BReAK_me_sPaCEbaR}**
  &nbsp;  
The main methods we used can be summarised as follows:
1. **Direct Geoguessr Techniques:** employ Geoguessr tools on one specific observation (a 'dead giveaway') to directly find the country.
2. **Indirect Geoguessr Techniques:** employ Geoguessr tools on several observations, to slowly narrow down the list of possible countries.
3. **Guess and Check:** use Google Maps streetview to see if the landscape/vibe of a country in question matches the image
4. **Contextual/ Meta Knowledge:** exploit knowledge about how these images are generated. We know all the images are from google maps streetview, so, for instance, we can look at the camera quality/ camera type/ date of the streetview image capture/ etc. for clues + any country that doesn't have streetview can be eliminated immediately
5. **Reverse Image Search**
6. (Meta-game)


  &nbsp;  

It's worth noting that these methods differ from the kind you may use as a Geoguessr player in a Geoguessr game. Hence it's worth keeping these in mind for any future Geoguessr-themed OSINT challenges.
