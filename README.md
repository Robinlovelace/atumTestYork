
The aim of this repo is to showcase ways of generating evidence to
support strategic active network planning tools in England and beyond.

The intention is to provide language agnostic description of input
datasets processes and functions for generating estimates of active
travel uptake down to the street level. It will make use of some of the
same input datasets that are used in the Propensity to Cycle Tool (PCT).
For full reproducibility, the code in this repo is developed in a Docker
container using the
[.devcontainer.json](https://containers.dev/implementors/json_reference/)
format.

We will cover input datasets, processing steps, and outputs.

# Input datasets

## Zone data

Zone data is available at many geographic levels, including large zones
(e.g. MSOAs) and small zones (e.g. Output Areas). MSOAs representing
York are shown below.

![](README_files/figure-commonmark/unnamed-chunk-3-1.png)

## Origin destination data

OD data has the following structure:

| geo_code1 | geo_code2 |  all | from_home | light_rail | train | bus | taxi | motorbike | car_driver | car_passenger | bicycle | foot | other | geo_name1          | geo_name2                | la_1           | la_2                 |
|:----------|:----------|-----:|----------:|-----------:|------:|----:|-----:|----------:|-----------:|--------------:|--------:|-----:|------:|:-------------------|:-------------------------|:---------------|:---------------------|
| E02000001 | E02000001 | 1506 |         0 |         73 |    41 |  32 |    9 |         1 |          8 |             1 |      33 | 1304 |     4 | City of London 001 | City of London 001       | City of London | City of London       |
| E02000001 | E02000014 |    2 |         0 |          2 |     0 |   0 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barking and Dagenham 013 | City of London | Barking and Dagenham |
| E02000001 | E02000016 |    3 |         0 |          1 |     0 |   2 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barking and Dagenham 015 | City of London | Barking and Dagenham |
| E02000001 | E02000025 |    1 |         0 |          0 |     1 |   0 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 002               | City of London | Barnet               |
| E02000001 | E02000028 |    1 |         0 |          0 |     0 |   0 |    0 |         0 |          1 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 005               | City of London | Barnet               |
| E02000001 | E02000051 |    1 |         0 |          1 |     0 |   0 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 028               | City of London | Barnet               |
| E02000001 | E02000053 |    2 |         0 |          2 |     0 |   0 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 030               | City of London | Barnet               |
| E02000001 | E02000057 |    1 |         0 |          1 |     0 |   0 |    0 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 034               | City of London | Barnet               |
| E02000001 | E02000058 |    1 |         0 |          0 |     0 |   0 |    0 |         0 |          0 |             0 |       0 |    1 |     0 | City of London 001 | Barnet 035               | City of London | Barnet               |
| E02000001 | E02000059 |    1 |         0 |          0 |     0 |   0 |    1 |         0 |          0 |             0 |       0 |    0 |     0 | City of London 001 | Barnet 036               | City of London | Barnet               |

## Data on origins and destinations

A key dataset type for simulating trips not covered by available OD data
is data on trip origins (e.g. representing residential areas and
population estimates) and ‘trip attractors’. These can be obtained from
OSM. These datasets typically have pont and polygon geometries and
numerous features that can feed into trip generation models, a
subsection of the enxt section.

# Processing steps

## Desire line generation

## Trip generation

## Jittering

## Routing

## Update functions

## Route network generation

## Visualisation

# Outputs
