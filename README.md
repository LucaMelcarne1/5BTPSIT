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
<ul>
      <li>It is easier to describe allowable document content</li>
      <li>It is easier to validate the correctness of data</li>
      <li>It is easier to define data facets (restrictions on data)</li>
      <li>It is easier to define data patterns (data formats)</li>
      <li>It is easier to convert data between different data types</li>
</ul>

<h4>Gli schemi XML utilizzano la sintassi XML</h4>
<p>Un altro grande punto di forza degli schemi XML è che sono scritti in XML.</p>
    <ul>
        <li>Non devi imparare una nuova lingua</li>
        <li>Puoi utilizzare il tuo editor XML per modificare i tuoi file Schema</li>
        <li>Puoi utilizzare il tuo parser XML per analizzare i tuoi file Schema</li>
        <li>Puoi manipolare il tuo schema con XML DOM</li>
        <li>Puoi trasformare il tuo schema con XSLT</li>
        <li>Gli schemi XML sono estensibili perché sono scritti in XML.</li>
    </ul>
<h4>Con una definizione di Schema estensibile puoi:</h4>
    <ul>
        <li>Riutilizza il tuo schema in altri schemi</li>
        <li>Crea i tuoi tipi di dati derivati ​​dai tipi standard</li>
        <li>Fare riferimento a più schemi nello stesso documento</li>
    </ul>

  <h4>XML Comunicazione dati sicura</h4> 
    <p>Quando si inviano dati da un mittente a un destinatario, è essenziale che entrambe le parti abbiano le stesse "aspettative" riguardo al contenuto.
    
        Grazie agli schemi XML, il mittente può descrivere i dati in un modo comprensibile per il destinatario.
        
        Una data come: "03-11-2004" verrà interpretata, in alcuni paesi, come 3 novembre e in altri come 11 marzo.
        
        Tuttavia, un elemento XML con un tipo di dati come questo:
        
        <date type="date">2004-03-11</date>
        
        garantisce una comprensione reciproca del contenuto, poiché il tipo di dati XML "data" richiede il formato "AAAA-MM-GG".</p>



