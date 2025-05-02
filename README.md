# 5BTPSIT
<h3>XML schema: introduction</h3>
<h4>What is an XML Schema?</h4>
<p>An XML Schema describes the structure of an XML document.</p>
<p>The XML Schema language is also referred to as XML Schema Definition (XSD).</p>
<p>XSD Example</p>

      <?xml version="1.0"?>
      <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
      <xs:element name="note">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="to" type="xs:string"/>
            <xs:element name="from" type="xs:string"/>
            <xs:element name="heading" type="xs:string"/>
            <xs:element name="body" type="xs:string"/>
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      </xs:schema>

<h4>Why Learn XML Schema? </h4>
<ul>
        <li>In the XML world, hundreds of standardized XML formats are in daily use. </li>
        <li>Many of these XML standards are defined by XML Schemas.</li>
        <li> XML Schema is an XML-based (and more powerful) alternative to DTD.</li>
</ul>
<h4>XML Schemas Support Data Types</h4>
<p>One of the greatest strength of XML Schemas is the support for data types.</p>
<ul>
      <li>It is easier to describe allowable document content</li>
      <li>It is easier to validate the correctness of data</li>
      <li>It is easier to define data facets (restrictions on data)</li>
      <li>It is easier to define data patterns (data formats)</li>
      <li>It is easier to convert data between different data types</li>
</ul>

<h4>XML Schemas use XML Syntax</h4>
<p>Another great strength about XML Schemas is that they are written in XML.</p>
    <ul>
        <li>You don't have to learn a new language</li>
        <li>You can use your XML editor to edit your Schema files</li>
        <li>You can use your XML parser to parse your Schema files</li>
        <li>You can manipulate your Schema with the XML DOM</li>
        <li>You can transform your Schema with XSLT</li>
    </ul>
<p>XML Schemas are extensible, because they are written in XML.</p>    
<p>With an extensible Schema definition you can:</p>
    <ul>
        <li>Reuse your Schema in other Schemas</li>
        <li>Create your own data types derived from the standard types</li>
        <li>Reference multiple schemas in the same document</li>
    </ul>


<h4>FILE studenti.xml</h4>

            <?xml version="1.0" encoding="UTF-8"?>
            <studenti xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                      xsi:noNamespaceSchemaLocation="studenti.xsd">
            
                <studente id="S001">
                    <cognome>Rossi</cognome>
                    <nome>Luca</nome>
                    <dataNascita>2005-04-15</dataNascita>
                    <sesso>M</sesso>
                    <città>Milano</città>
                    <prov>MI</prov>
                    <email>luca.rossi@example.com</email>
                </studente>
            
                <studente id="S002">
                    <cognome>Bianchi</cognome>
                    <nome>Anna</nome>
                    <dataNascita>2004-11-02</dataNascita>
                    <sesso>F</sesso>
                    <città>Torino</città>
                    <prov>TO</prov>
                    <telefono>0111234567</telefono>
                </studente>
            
                <studente id="S003">
                    <cognome>Verdi</cognome>
                    <nome>Marco</nome>
                    <dataNascita>2003-07-23</dataNascita>
                    <sesso>M</sesso>
                    <città>Firenze</città>
                    <prov>FI</prov>
                    <email>marco.verdi@example.com</email>
                    <telefono>0557654321</telefono>
                </studente>
            
            </studenti>

<h4>FILE studenti.xsd</h4>
                  
                  <?xml version="1.0" encoding="UTF-8"?>
                  <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
                    <xs:element name="studenti">
                      <xs:complexType>
                        <xs:sequence>
                          <xs:element name="studente" maxOccurs="unbounded">
                            <xs:complexType>
                              <xs:sequence>
                                <xs:element name="cognome" type="xs:string"/>
                                <xs:element name="nome" type="xs:string"/>
                                <xs:element name="dataNascita" type="xs:date"/>
                                <xs:element name="sesso">
                                  <xs:simpleType>
                                    <xs:restriction base="xs:string">
                                      <xs:enumeration value="M"/>
                                      <xs:enumeration value="F"/>
                                    </xs:restriction>
                                  </xs:simpleType>
                                </xs:element>
                                <xs:element name="città" type="xs:string"/>
                                <xs:element name="prov">
                                  <xs:simpleType>
                                    <xs:restriction base="xs:string">
                                      <xs:pattern value="[A-Z]{2}"/>
                                    </xs:restriction>
                                  </xs:simpleType>
                                </xs:element>
                                <xs:element name="email" type="xs:string" minOccurs="0"/>
                                <xs:element name="telefono" type="xs:string" minOccurs="0"/>
                              </xs:sequence>
                              <xs:attribute name="id" type="xs:string" use="required"/>
                            </xs:complexType>
                          </xs:element>
                        </xs:sequence>
                      </xs:complexType>
                    </xs:element>
                  
                  </xs:schema>
            


