# The dataset regarding the vaccination drive in the different regions of United States 


## Number of Country Regions 
```SQL 
SELECT count( country_region_code)FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  LIMIT 1000
```
Ans: 477861

## Number of cities in Sub region 1, 2 and 3 
```SQL
SELECT count(sub_region_1)FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  LIMIT 1000
```
Ans: 477828
```SQL
SELECT count(sub_region_2)FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  LIMIT 1000
```
Ans: 475591
```SQL
SELECT count(sub_region_3)FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  LIMIT 1000
```
Ans: 379347

## What is the timeframe of the dataset or when was the first and the last vaccination status of 2021 recorded?
```
SELECT min(date) as initial_date
,max(date) as final_date 
FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  LIMIT 1000
```
Ans: 	initial_date          final_date	
     
      2021-01-04             2021-08-16

## What percentage of people faced side effects of the vaccination?
```SQL
SELECT AVG(sni_safety_side_effects) AS SIDE_EFFECTS, country_region
FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights`  
GROUP BY country_region
```
Ans:      SIDE_EFFECTS	               country_region	
      
        11.415198669190064             United States

 ## What is the Percentage of vaccinated population in the sub region 2?
```SQL
SELECT AVG(sni_covid19_vaccination) AS VACCINATION ,sub_region_2 
FROM `bigquery-public-data.covid19_vaccination_search_insights.covid19_vaccination_search_insights` 
GROUP BY sub_region_2
```
Ans:      VACCINATION                      sub_region_2	
      
         35.3862158054711                   Pike County
	
       38.25709523809523                   Kiowa County

       33.74845                            Lyman County

       52.192183079056846                  Pinal County

       57.49137995337998                   Livingston County

       47.179656249999994                  Teton County

       55.4226795302014                    Beaver County

      28.503208333333333                   Cherry County

      39.24743939393941                    Huron County
	
      61.76071341463413                    Buncombe County
	
      32.65475757575758                    Orangeburg County
	
      65.20233333333333                    Addison County
	
      36.57532290184922                    Lincoln County
	
      64.97907792207798                    Harford County

      52.891606132075516                   Martin County
	
      45.6889333333333                    Knox County
	
      25.25830303030303                   Young County
	
      26.33730303030303                   Apache County
	
      52.82081590377553                  Hamilton County
	
     44.851635259631536                  Madison County

     55.668470191226056                  Collin County
	
     55.3868787878788                    St. Louis
	
     62.64754102153403                  Montgomery County

     44.762273266153045                 Wayne County
	
     30.8708383838384                   Coffee County
	
     29.993272727272725                 Dent County

     34.45148484848485                 Pottawatomie County
	
     37.09369696969698                 Meeker County
	
     61.07401677704185                 null
	
     72.41397175141257                Howard County
	
     43.83252950819673                Clay County
	
     36.9159393939394                 Montezuma County
	
     27.871437499999995              Conecuh County
	
     56.44887878787878               Routt County
	
     37.36204268292683               Johnston County

     31.294246153846167              Russell County
	
     36.4090606060606               Christian County

     39.186818181818175             Hubbard County
	
     50.059357247976436             Franklin County

     43.91740140845069              Columbia County
	
     55.96133333333334              Poquoson
	
     20.60321212121212              McKenzie County

     29.12736363636364              St. Landry Parish

     40.68021052631578              Kingsbury County
	
     35.822906666666654             Marshall County
	
     36.465424242424234             Caldwell County

     34.734106508875726             Jones County
	
     31.506999999999998             Norman County

     49.47787878787878             Isle of Wight County
	
     39.53536363636365             Whiteside County

     52.41618181818181             Door County
	
     42.79724242424241             Amherst County
    
     41.7929690026954              Brown County

     41.87448484848484             Rockdale County

     20.803454545454542            Scurry County
	
     26.410357142857144            Desha County
	
     61.37387084148725             Larimer County

     51.11495908825238             Kent County

    43.541979020978985             Putnam County

    45.73258823529413              Stafford County

    42.09082857142857              Cameron County
	
    28.489749999999994             Lemhi County
	
    33.49716666666666              Lac qui Parle County
	
    38.50939215686272              Yuma County

    51.12290761223156              Fayette County

    47.22421117841411              Clark County
	
    26.761684210526315             Todd County
	
    35.9791212121212               Silver Bow County
	
    73.2965474747475               Hudson County
	
    33.56633333333333              Matagorda County
	
    33.49245454545454              Sequatchie County
	
    36.70330303030302              McClain County
	
    52.84929765545358              Spokane County

    42.747485499463025             Pulaski County

    33.91188                       Barber County
	
   54.82077581863981               Maui County
	
   35.21939393939393               Defiance County
	
   29.408937500000004              Cameron Parish

   41.34127272727273               Sanilac County
	
   50.3976923076923                Tensas Parish
	
   33.467745454545444              Lyon County

   47.585366442953045              Polk County
	
   40.03656380208338               Cass County
	
   46.721796733741584              Jackson County
	
   36.62527272727272               Tallapoosa County

   57.75248291113796               York County

   48.65990909090909               Josephine County
	
   53.80841212121208               Fulton County

   55.46845454545454               Story County
	
   37.33574193548388               Delta County
	
   48.535671080508415              Jefferson County

   41.58054545454546               Prince Edward County
	
   74.74956851119894               Fairfax County
	
   34.06975793650792               Logan County
	
   57.86710997114459               Monroe County
	
   33.14115151515151               Van Zandt County
	
   52.156506751389955              Butler County
	
   46.881575757575746              Wallowa County
	
   39.885924242424245              Roane County
	
   34.76357575757576               Churchill County






