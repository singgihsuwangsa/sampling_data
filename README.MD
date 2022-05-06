## Sampling weather data

Mendownload sebuah file excel dari link berikut dan menyimpannya di dalam folder sampling_data:
`wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx`

Mengubah format sheet pertama dari xlsx menjadi csv:
`in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv`

Mengubah format sheet kedua dari xlsx menjadi csv:
`in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv`

Gabungkan data weather_2014 dan weather_2015 menjadi satu file weather.csv. Selain itu hapus file weather_data.xlsx:
`csvstack weather_2014.csv weather_2015.csv > weather.csv | rm weather_data.xlsx`

Lakukan sampling pada file weather.csv dengan rate 0.3 kemudian simpan kedalam file sample_weather.csv:
`sample -r 0.3 weather.csv > sample_weather.csvn2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv`
