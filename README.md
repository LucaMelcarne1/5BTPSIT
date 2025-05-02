# 5BTPSIT
<h3>Argomento: XML schema</h3>
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

It is easier to describe allowable document content
It is easier to validate the correctness of data
It is easier to define data facets (restrictions on data)
It is easier to define data patterns (data formats)
It is easier to convert data between different data types




