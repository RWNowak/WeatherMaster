# WeatherMaster
A simple app for checking the weather

# Dokumentacja aplikacji WeatherMaster
## Opis
WeatherMaster to aplikacja mobilna napisana w języku Java przy użyciu Android Studio. Aplikacja umożliwia uzyskanie informacji o pogodzie na podstawie wprowadzonej nazwy miejsca. Korzysta z API OpenWeatherMap do pobierania danych o pogodzie.

##Struktura projektu
Aplikacja składa się z jednego pliku Java o nazwie MainActivity.java. W pliku tym znajduje się implementacja interfejsu użytkownika oraz logika biznesowa związana z pobieraniem danych o pogodzie.

## Zależności
Aplikacja wykorzystuje bibliotekę Volley do wykonywania żądań HTTP. W pliku build.gradle znajduje się deklaracja zależności dla tej biblioteki.

implementation 'com.android.volley:volley:1.2.1'

## Interfejs użytkownika
Aplikacja składa się z jednego ekranu, który zawiera trzy elementy interfejsu użytkownika:

Pole tekstowe do wprowadzania nazwy miasta (etCity)
Pole tekstowe do wprowadzania nazwy kraju (etCountry)
Pole tekstowe wyświetlające wyniki dotyczące pogody (tvResult)

## Logika aplikacji
Po wprowadzeniu nazwy miasta i kraju, użytkownik może nacisnąć przycisk, który wywołuje metodę GetWeatherDetails(View view). Metoda ta pobiera wprowadzone przez użytkownika wartości z pól tekstowych, tworzy odpowiedni URL i wykonuje żądanie HTTP za pomocą biblioteki Volley do API OpenWeatherMap.

Po otrzymaniu odpowiedzi z serwera, dane dotyczące pogody są przetwarzane i wyświetlane w polu tekstowym tvResult. Informacje o pogodzie obejmują temperaturę, odczuwalną temperaturę, wilgotność, opis, prędkość wiatru, zachmurzenie i ciśnienie atmosferyczne.

W przypadku błędu podczas pobierania danych o pogodzie, zostaje wyświetlony stosowny komunikat błędu.

## Użyte API
Aplikacja korzysta z następującego API:

OpenWeatherMap: API dostarcza informacje o pogodzie na podstawie wprowadzonej nazwy miejsca. Adres URL do pobierania danych to https://api.openweathermap.org/data/2.5/weather. Aplikacja wymaga klucza API do uwierzytelnienia, który jest przekazywany poprzez parametr appid w żądaniu.

## Dodatkowe informacje
Temperatura jest wyrażana w stopniach Celsiusza.
Prędkość wiatru jest wyrażana w metrach na sekundę (m/s).
Zachmurzenie jest wyrażane w procentach (%).
Ciśnienie atmosferyczne jest wyrażane w hektopaskalach (hPa).
