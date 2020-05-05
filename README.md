## Intro

Here you can find the latest and most successful version of our attempt to predict car prices in InClass competition hosted by SkillFactory (to find out more go to: https://www.kaggle.com/c/sf-dst-car-price/overview).

The solution kit consists of:
- a multithreaded scrapper to collect data, needed for model training;
- train and test data to feed into the script;
- a script in which the data is beautifully adjusted, preprocessed and the model is built.

## Scrapper

**Involves scrapper itself, add-on mark-model dictionary**

In the competition there were no preprepared training data, and we were suggested to collect it by ourselves, according to the test dataset.
First, using test data we checked, what are the car brands we will work with.
We also new that all the information was gathered from auto.ru web-site. On the bases of its sitemap we made a dictionary with brands as the keys and models as values (corresponding code and dictionary are included).
The scrapper then uses this dictionary to find advertisements for each model, adds needed information to another dictionary and dumps it all into a file in the end.
Information for training dataset was collected almost every day during the competition period, which helped us among other thing to get better results.

## Data

**This folder contains three files:
-(train file path)
-(test file path)
-(sample submission file path)**

Both train and test data include the following features:

```bodyType``` - the body type of a car

```brand``` - car brand name

```color``` - the color of a car

```fuelType``` - car fuel type

```modelDate``` - the year of the car model release

```name``` - contains information from several other columns (engineDisplacement, enginePower) plus some piece of a model reference, but not in every case

```numberOfDoors``` - the number of doors in the car

```productionDate``` - the year when a particular car was produced

```vehicleConfiguration``` - the configuration of a car

```vehicleTransmission``` - the type of vehicle transmission of a car

```engineDisplacement``` - the engine displacement of a car

```enginePower``` - the power of car engine

```description``` - owner description to the advertisement

```mileage``` - the total distance, travelled by a car 

```Комплектация``` - a list of car equipment

```Привод``` - the type of a drivegear

```Руль``` - the side on which the driving wheel is located

```Состояние``` - the condition of a car

```Владельцы``` - the number of car owners

```ПТС``` - the type of car documents (original or duplicate)

```Таможня``` - if the car was customs cleared

```Владение``` - the ownership period for the last owner

There is also a sample of submission for Kaggle, which should be filled in with price values, predicted by the model, saved and submitted to the competition.
