---
title: XSLT
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 733dd62122ee99d4e243c2af724f709a15333d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474658"
---
# <a name="xslt-transformations"></a>XSLT


**Betrifft**: Access 2013 | Office 2013

## <a name="xslt-transformations"></a>XSLT

XSLT kann auf den generierten XML-Code angewandt werden, um ihn in ein anderes Format zu transformieren. Die Kenntnis des XML-Formats in ADO hilft bei der Entwicklung von XSLT-Vorlagen, mit denen die Transformierung in ein benutzerfreundlicheres Format möglich ist.

Beispielsweise wissen Sie, dass jede Zeile des Recordset-Objekts als z:row-Element im rs:data-Element gespeichert wird. Entsprechend wird jedes Feld des Recordset-Objekts als Attribut/Wert-Paar für dieses Element gespeichert.

Das folgende XSLT-Skript kann auf den im vorherigen Abschnitt gezeigten XML-Code angewandt werden, um ihn in eine HTML-Tabelle zu transformieren, die im Browser angezeigt wird:

```xml 
 
<?xml version="1.0" encoding="ISO-8859-1"?> 
<html xmlns:xsl="https://www.w3.org/TR/WD-xsl"> 
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white"> 
<table border="1" style="table-layout:fixed" width="600"> 
  <col width="200"></col> 
  <tr bgcolor="teal"> 
    <th><font color="white">CustomerId</font></th> 
    <th><font color="white">CompanyName</font></th> 
    <th><font color="white">ContactName</font></th> 
  </tr> 
<xsl:for-each select="xml/rs:data/z:row"> 
  <tr bgcolor="navy"> 
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td> 
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td> 
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>  
  </tr> 
</xsl:for-each> 
</table> 

</body> 
</html> 
```

XSLT konvertiert den von der **Save** -Methode von ADO generierten XML-Datenstrom in eine HTML-Tabelle, in der jedes Feld des **Recordset** -Objekts zusammen mit einer Tabellenüberschrift angezeigt wird. Tabellenüberschriften und Zeilen werden außerdem unterschiedliche Schriftarten und Farben zugewiesen.

