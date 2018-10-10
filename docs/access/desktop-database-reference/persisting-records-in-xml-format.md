---
title: Speichern von Datensätzen im XML-Format
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b1e22c3f85c4289520326c34c6d0c218a442a3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474501"
---
# <a name="persisting-records-in-xml-format"></a>Speichern von Datensätzen im XML-Format


**Betrifft**: Access 2013 | Office 2013

Das Speichern von Recordset-Objekten im XML-Format wird wie beim ADTG-Format mit dem Microsoft OLE DB-Anbieter für Persistenz implementiert. Dieser Provider generiert ein schreibgeschütztes Vorwärtsrowset von einer gespeicherten XML-Datei oder einem gespeicherten XML-Datenstrom, die bzw. der die von ADO generierten Schemainformationen enthält. Entsprechend kann damit ein Recordset-Objekt von ADO verwendet, XML generiert sowie in einer Datei oder einem beliebigen Objekt gespeichert werden, das die COM-Schnittstelle IStream implementiert. (Eine Datei ist lediglich ein weiteres Beispiel für ein Objekt, das IStream unterstützt.) Für die Versionen 2.5 und höher verwendet ADO den Microsoft XML Parser (MSXML), um den XML-Code in das Recordset-Objekt zu laden. Deshalb ist msxml.dll erforderlich. Für Version 2.5 wurde MSXML mit Internet Explorer 5 ausgeliefert. Für Version 2.6 wurde MSXML mit SQL Server 2000 ausgeliefert.


> [!NOTE]
> <P>[!HINWEIS] Beim Speichern hierarchischer <STRONG>Recordset</STRONG> -Objekte (Datenstrukturen) im XML-Format gelten einige Einschränkungen. Das Speichern im XML-Format ist nicht möglich, wenn das hierarchische <STRONG>Recordset</STRONG> -Objekt ausstehende Aktualisierungen aufweist. Außerdem kann ein parametrisiertes hierarchisches <STRONG>Recordset</STRONG> -Objekt nicht gespeichert werden. Weitere Informationen finden Sie unter <A href="hierarchical-recordsets-in-xml.md">Hierarchische Recordset-Objekte in XML</A>.</P>



Die Save-Methode bzw. die Open-Methode sind die einfachste Möglichkeit, um Daten im XML-Format zu speichern und über ADO erneut zu laden. Das folgende ADO-Codebeispiel veranschaulicht, wie die Daten in der Titles-Tabelle in der Datei titles.sav gespeichert werden.

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

ADO speichert stets das gesamte **Recordset** -Objekt. Wenn Sie nur eine Teilmenge der Zeilen des **Recordset** -Objekts beibehalten möchten, verwenden Sie die **Filter** -Methode die Zeilen Identitätswerte oder Ändern Ihrer Auswahlklausel. Sie müssen jedoch ein **Recordset** -Objekt mit einem clientseitige Cursor öffnen (**CursorLocation** = **AdUseClient**) mit der **Filter** -Methode zum Speichern einer Teilmenge von Zeilen. Um Titel abzurufen, die mit dem Buchstaben "b" beginnen, können Sie beispielsweise einen Filter auf ein geöffnetes **Recordset** -Objekt anwenden:

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

ADO verwendet stets das Client Cursor Engine-Rowset, um neben den vom Anbieter für Persistenz generierten Vorwärtscursordaten ein **Recordset** -Objekt zu erstellen, für das der Fensterinhalt verschoben und Lesezeichen festgelegt werden können.

