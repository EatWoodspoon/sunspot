## What
This is fork of https://github.com/sunspot/sunspot is because the `sunspot_solr` gem does not include the library that solr depends on for spatial searching, JTS. 

Our Rails app was using the spatial capabilities of solr, and we encountered this error when trying to run solr locally using `rake sunspot:solr:run`: 
```
java.lang.NoClassDefFoundError: com/vividsolutions/jts/geom/CoordinateSequenceFactory
```

This fork is suppose to solve it. 

## Usage

in your gemfile, replace:
```
  gem 'sunspot_solr'
```
With:
```
  gem 'sunspot_solr', :git => 'git://github.com/EatWoodspoon/sunspot.git'
```
