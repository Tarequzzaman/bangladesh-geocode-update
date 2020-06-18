# bangladesh-geocode-update


<p>In this project everything like Division, District, Upazila, Union connected via ID. I have collected the geo location from  <a href="http://app.dghs.gov.bd/bbscode/pages/divReport/">here</a>. 
The location info lat & long are provided on district lavel. You can also contribute to find the lat, long for upazila, union etc. 
</p>

Below I have added the usages of this json files: 


1. Read the json files 

   
   Read the division
   
   ```python
      division= []
      with open('division.json') as f:
           division = json.load(f)
   ```
   Output <br>
   ```
    [{'Division Code': '40', 'Division': 'Khulna'},
    {'Division Code': '20', 'Division': 'Chittagong'},
    {'Division Code': '10', 'Division': 'Barisal'},
    {'Division Code': '50', 'Division': 'Rajshahi'},
    {'Division Code': '30', 'Division': 'Dhaka'},
    {'Division Code': '55', 'Division': 'Rangpur'},
    {'Division Code': '60', 'Division': 'Sylhet'},
    {'Division Code': '65', 'Division': 'Mymensingh'}]
   ```
   <br>

  
   Read the District
   
   ```python
      division= []
      with open('district.json') as f:
           division = json.load(f)
   ```
   Output <br>
   ```
    [{'Division Code': '40',
    'District': 'Bagerhat',
    'District code': '1',
    'lat': '22.651568',
    'long': '89.785938'},
    {'Division Code': '20',
    'District': 'Bandarban',
    'District code': '3',
    'lat': '22.1953275',
    'long': '92.2183773'},
    {'Division Code': '10',
    'District': 'Barguna',
    'District code': '4',
    'lat': '22.0953',
    'long': '90.1121'},
    . 
    . 
      

    . 
    . 
    ]
   ```



2. Find all district from the dhaka division (Python)

```python 


```