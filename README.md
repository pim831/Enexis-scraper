# Enexis-scraper
Python script (Electric_net_scraper.py) for scraping the electric net capacity of Dutch postal codes from https://www.enexis.nl/zakelijk/aansluitingen/elektriciteit-terugleveren/beperkte-capaciteit-op-het-elektriciteitsnet?postalcode=#capaciteitcheck.
The information was retreived by looping over a list of available postal code ranges for the Netherlands (postal_codes.txt), which was retreived from https://nl.wikipedia.org/wiki/Postcodes_in_Nederland.
The scraper sends a request to the enexis web tool for the first entry (AA) of each postal code and then stores the (Dutch) color coding of that postal code [ROOD=no transport capacity, ORANJE=minimal transport capacity, GEEL= limitations on the transport capacity, WIT=transport capacity available].
After the data is collected for all postal codes the postal_codes_cleaner.py script can be used to clean the data (throw out all the postal codes for which no info was available).
