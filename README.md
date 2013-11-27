jiac-gpx-facts
==============

Provides a JIAC V compatible facts representation & import of GPX 1.1 data.

The Facts are generated using XJB. Dates are represented in Joda-Time. If the date is not parseable, it is set to null.

Importing can be as simple as
```java
JAXBContext context = JAXBContext.newInstance("de.effms.jiactng.facts.gpx");
Unmarshaller unmarshaller = context.createUnmarshaller();
JAXBElement result = (JAXBElement) unmarshaller.unmarshal(new StringReader(this.contents));
GpxType x = (GpxType) result.getValue();
```

This artifact is available in this GitHub Repository: https://github.com/fritz-gerneth/dev-maven-repo
