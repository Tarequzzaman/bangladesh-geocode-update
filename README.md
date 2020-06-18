# bangladesh-geocode-update


<p>In this project everything like Division, District, Upazila, Union connected via ID. I have collected the geo location from  <a href="http://app.dghs.gov.bd/bbscode/pages/divReport/">here</a>. 
The location info lat & long are provided on district lavel. You can also contribute to find the lat, long for upazila, union etc. 
</p>

Below I have added the usages of this json files on python: 


1. Read the json files: 

   
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
    ]
    ```
    Read the Upazilas
   
   ```python
        upazila= []
        with open('upazila.json') as f:
            upazila = json.load(f)
   ```
   Output <br>
   ```
    [{'District code': '1', 'Upazilla': 'Bagerhat Sadar', 'Upazilla Code': '8'},
    {'District code': '1', 'Upazilla': 'Mongla', 'Upazilla Code': '58'},
    {'District code': '1', 'Upazilla': 'Morrelganj', 'Upazilla Code': '60'},
    {'District code': '3', 'Upazilla': 'Bandarban Sadar', 'Upazilla Code': '14'},
    {'District code': '3', 'Upazilla': 'Lama', 'Upazilla Code': '51'},
    {'District code': '4', 'Upazilla': 'Amtali', 'Upazilla Code': '9'},
    {'District code': '4', 'Upazilla': 'Barguna Sadar', 'Upazilla Code': '28'},
    {'District code': '4', 'Upazilla': 'Betagi', 'Upazilla Code': '47'},
    . 
    . 
    ]
   ```
    Read the Unions
   
   ```python
        unions= []
        with open('union-word.json') as f:
            unions = json.load(f)
   ```
   Output <br>
   ```
    [{'Upazilla Code': '8', 'Union-Word': 'Ward No-01', 'Union Code': '1'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-02', 'Union Code': '2'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-03', 'Union Code': '3'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-04', 'Union Code': '4'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-05', 'Union Code': '5'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-06', 'Union Code': '6'},
    {'Upazilla Code': '8', 'Union-Word': 'Ward No-07', 'Union Code': '7'},
    . 
    . 
    ]
   ```


2. Find all district from the dhaka division (Python)

 <p>From the output of Division the <strong>'Division Code': '30'</strong></p>

    ```python 
    dhaka_district=[]

        for d in district:
            if(d['Division Code']=='30'):
                dhaka_district.append(d)
    ```

 Output <br>


    ```
    [{'Division Code': '30',
    'District': 'Dhaka',
    'District code': '26',
    'lat': '23.7115253',
    'long': '90.4111451'},
    {'Division Code': '30',
    'District': 'Faridpur',
    'District code': '29',
    'lat': '23.6070822',
    'long': '89.8429406'},
    {'Division Code': '30',
    'District': 'Gazipur',
    'District code': '33',
    'lat': '24.0022858',
    'long': '90.4264283'},
    .
    .
    ]

    ```