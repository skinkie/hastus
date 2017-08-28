Giro Hastus export to NeTEx
===========================

This repository contains a Giro Hastus (2014/2016) export for Hastus to the Dutch NeTEx profile.

Requirements
------------

Your Hastus installation contains a hastus.ini configuration, you should add or check the following section. This will allow runtime patterns to be specific to stop (value 1) instead of place (value 0, the default). Before changing this value remove the existing runtime patterns.

```
[RPAT]
RPAT_DEFINE_BY = 1
RPAT_USE_OFFSRV = TRUE
```

This script uses runtime patterns, you must generate them for the export to work.

Configuration
-------------

Due to the nature of OIG processing not all configuration appears in Configuratie.ix because every conditional branch in OIG processing seem to be computed.
Therefore some intensive scripts must be switch on/off manually:

	CompositeFrame/ResourceFrame/typesOfValue.ix (Arriva tariffStop)
	CompositeFrame/ServiceFrame/tariffZones.ix (Arriva tariffStop)

	CompositeFrame/ServiceFrame.ix (Hastus 2014/2016 routePoints, Route/Itinerary based routeLinks)


