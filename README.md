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


<p>The purpose of an XML Schema is to define the legal building blocks of an XML document: </p>
<li>
        <ul>the elements and attributes that can appear in a document </ul></li>
        <ul> the number of (and order of) child elements</ul>
        <ul> data types for elements and attributes</ul>
        <ul> default and fixed values for elements and attributes</ul>
</li>





