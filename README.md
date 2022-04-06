# Accidents
 
It is an XML and a XML Schema of the accidents occured in Gran Canaria during 2014 aproximately.

There is a folder called GithubProyect that has some screenshots of the XML and its validation

### IMPORTANT:

### Screenshots

* Creating the XML:

![create product](https://github.com/JohanSantanaGalvan/Accidents/blob/main/GithubProyect/XML.PNG)

* Creating the XSD:

![show products](https://github.com/JohanSantanaGalvan/Accidents/blob/main/GithubProyect/XSD.PNG)

### Prerequisites

Before starting you need to install Visual Studio Code and then the XML extension. Check the links bellow.

### XML and XSD files 

An example of XML file sent from client to web service to create a new product:

```
<?xml version="1.0" encoding="UTF-8"?>
<data>
   <row _id="1">
     <DILIG>2</DILIG>
     <PLACE>SERVENTIA Nº 326</PLACE>
     <HEIGHT_OF />
     <DATE>2014-01-01T00:00:00</DATE>
     <HOUR>03:20</HOUR>
     <VEHICLES>1</VEHICLES>
     <INJURED>2</INJURED>
     <DESTINATION>Juzgado</DESTINATION>
     <COLLISION>Otros</COLLISION>
     <INFR_COND>Inexperiencia del conductor</INFR_COND>
     <INFR_PEAT>Ninguna infracción</INFR_PEAT>
     <COMPLAINTS>0</COMPLAINTS>
   </row>
</data>
```

An example of XML file stored in the Server:

```
<?xml version="1.0" encoding="UTF-8"?>
<data>
   <row _id="1">
     <DILIG>2</DILIG>
     <PLACE>SERVENTIA Nº 326</PLACE>
     <HEIGHT_OF />
     <DATE>2014-01-01T00:00:00</DATE>
     <HOUR>03:20</HOUR>
     <VEHICLES>1</VEHICLES>
     <INJURED>2</INJURED>
     <DESTINATION>Juzgado</DESTINATION>
     <COLLISION>Otros</COLLISION>
     <INFR_COND>Inexperiencia del conductor</INFR_COND>
     <INFR_PEAT>Ninguna infracción</INFR_PEAT>
     <COMPLAINTS>0</COMPLAINTS>
   </row>
</data>
```

XSD file in Server:

```
<?xml version="1.0" encoding="UTF-8"?>

<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" targetNamespace="https://www.w3schools.com" xmlns="https://www.w3schools.com" elementFormDefault="qualified">
  <xs:element name="data">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="row" minOccurs="1" maxOccurs="unbounded" type="rowType"></xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>

  <xs:complexType name="rowType">
      
    <xs:sequence>
      <xs:element name="DILIG" type="xs:positiveInteger" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="PLACE" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="HEIGHT_OF" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="DATE" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="HOUR" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="VEHICLES" type="xs:integer" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="INJURED" type="xs:integer" minOccurs="0" maxOccurs="unbounded"></xs:element>
      <xs:element name="DESTINATION" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="COLLISION" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="INFR_COND" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="INFR_PEAT" type="xs:string" minOccurs="1" maxOccurs="unbounded"></xs:element>
      <xs:element name="COMPLAINTS" type="xs:integer" minOccurs="1" maxOccurs="unbounded"></xs:element>
</xs:sequence>
<xs:attribute name="_id" type="xs:positiveInteger"></xs:attribute>
</xs:complexType>

</xs:schema>
```

# Validation screenshots

A validation test offline made with Visual Studio Code. 

![validation test](https://github.com/JohanSantanaGalvan/Accidents/blob/main/GithubProyect/XML%20Validation.PNG)

## Built With

* [Visual-Studio-Code](https://code.visualstudio.com) - The System that I have used to create the code.
* [xsd-schema-validator](https://www.npmjs.com/package/xsd-schema-validator) - Allows XML validation with an XML Schema.


## Acknowledgments

* https://gist.github.com/PurpleBooth/109311bb0361f32d87a2#file-readme-template-md. A very good Readme.md template.
* https://www.w3schools.com/xml/schema_intro.asp. Understanding the XSD is a must for anyone working with XML. You can learn a lot with this tutorial.
* http://datosabiertos.laspalmasgc.es/resource/?ds=atestados-policia-local-2014&id=999fbede-ec95-4493-9e5b-4d9806a5e103&ft=XML. The open Data Source
