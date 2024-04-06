# COVID19 Air Traffic Data
Data processing of OpenSky COVID-19 Flight Dataset

## About [OpenSky COVID-19 Flight Dataset](https://opensky-network.org/community/blog/item/6-opensky-covid-19-flight-dataset)

The data in this dataset is derived and cleaned from the full OpenSky dataset to illustrate the development of air traffic during the COVID-19 pandemic. It spans all flights seen by the network's more than 2500 members between 1 January 2020 and 1 May 2020. More data will be periodically included in the dataset until the end of the COVID-19 pandemic.

### Disclaimer

The data provided in the files is provided as is. Despite best efforts at filtering out potential issues, some information could be erroneous.

- Origin and destination airports are computed online based on the ADS-B trajectories on approach/takeoff: no crosschecking with external sources of data has been conducted.
Fields origin or destination are empty when no airport could be found.
- Aircraft information come from the OpenSky aircraft database. Fields typecode and registration are empty when the aircraft is not present in the database.

### Description of the dataset

One file per month is provided as a csv file with the following features:

- callsign: the identifier of the flight displayed on ATC screens (usually the first three letters are reserved for an airline: AFR for Air France, DLH for Lufthansa, etc.)
- number: the commercial number of the flight, when available (the matching with the callsign comes from public open API)
- icao24: the transponder unique identification number;
- registration: the aircraft tail number (when available);
- typecode: the aircraft model type (when available);
- origin: a four letter code for the origin airport of the flight (when available);
- destination: a four letter code for the destination airport of the flight (when available);
- firstseen: the UTC timestamp of the first message received by the OpenSky Network;
- lastseen: the UTC timestamp of the last message received by the OpenSky Network;
- day: the UTC day of the last message received by the OpenSky Network.

## Data explorer

[Raw OpenSky Data](/opensky_data)

Flight data by countries: [CSV](/flight_data/flights.csv), [Excel](/flight_data/flights.xlsx)

## Data processing script

[Jupyter Notebook](Air%20Traffic.ipynb) with detailed comments

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Credit

Matthias Schäfer, Martin Strohmeier, Vincent Lenders, Ivan Martinovic and Matthias Wilhelm.
"Bringing Up OpenSky: A Large-scale ADS-B Sensor Network for Research".
In Proceedings of the 13th IEEE/ACM International Symposium on Information Processing in Sensor Networks (IPSN), pages 83-94, April 2014.
