---
title: Record-Objekt (ADO)
TOCTitle: Record object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 96ddc7fc1a93543f0eea2b42a3d423ec25a00636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300903"
---
# <a name="record-object-ado"></a>Record-Objekt (ADO)


**Gilt für**: Access 2013, Office 2013

Stellt eine Zeile aus einem [Recordset](recordset-object-ado.md)-Objekt oder des Data Providers dar oder ein Objekt, das von einem halbstrukturierten Data Provider zurückgegeben wird, wie etwa eine Datei oder ein Verzeichnis.

## <a name="remarks"></a>Bemerkungen

Ein **Record** -Objekt stellt eine Datenzeile dar und hat konzeptuelle Ähnlichkeiten mit einem einzeiligen **Recordset** -Objekt. Abhängig von den Fähigkeiten des Anbieters können **Record** -Objekte vom Anbieter anstatt eines einzeiligen **Recordset** -Objekts direkt zurückgegeben werden, z. B. wenn eine SQL-Abfrage ausgeführt wird, die nur eine Zeile auswählt. Ein **Record** -Objekt kann auch direkt von einem **Recordset** -Objekt erhalten werden. Ebenso kann ein **Record** -Objekt direkt von einem Anbieter an halbstrukturierte Daten zurückgegeben werden, wie etwa den OLE DB-Anbieter für Microsoft Exchange.

Sie können die Felder, die dem **Record** -Objekt zugeordnet sind, mithilfe der [Fields](fields-collection-ado.md)-Auflistung des **Record** -Objekts anzeigen. ADO lässt Spalten mit Objektwerten, einschließlich **Recordset** -, **SafeArray** - und skalaren Werten, in der **Fields** -Auflistung des **Record** -Objekts zu.

Wenn das **Record** -Objekt eine Zeile in einem **Recordset** -Objekt darstellt, ist es möglich, mit der **Source**-Eigenschaft zu diesem ursprünglichen [Recordset](source-property-ado-record.md) -Objekt zurückzukehren.

Das **Record** -Objekt kann auch von halbstrukturierten Data Providern, wie etwa dem [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), zum Anlegen von strukturierten Namespaces verwendet werden. Jeder Knoten in der Baumstruktur ist ein **Record** -Objekt mit zugeordneten Spalten. Die Spalten können die Attribute des Knotens und andere relevante Informationen darstellen. Das **Record** -Objekt kann sowohl einen Blattknoten als auch einen Nicht-Blattknoten in der Baumstruktur darstellen. Nicht-Blattknoten haben weitere Knoten zum Inhalt, während Blattknoten keine solchen Inhalte haben. Blattknoten enthalten typischerweise binäre Datenströme, während Nicht-Blattknoten auch ein Standarddatenstrom zugeordnet sein kann. Der Knotentyp wird durch Eigenschaften des **Record** -Objekts identifiziert.

Das **Record** -Objekt ist auch eine alternative Möglichkeit, in hierarchisch organisierten Daten zu navigieren. Ein **Record** -Objekt kann als Wurzel in einer großen Baumstruktur erstellt werden, und neue **Record** -Objekte können als untergeordnete Knoten geöffnet werden.

Eine Ressource (z. B. eine Datei oder ein Verzeichnis) kann durch eine absolute URL eindeutig identifiziert werden. Wenn das **Record**-Objekt mit einer absoluten URL geöffnet wird, wird implizit ein [Connection](connection-object-ado.md)-Objekt erstellt und auf das **Record**-Objekt festgelegt. Ein **Connection**-Objekt kann mit der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft explizit auf das **Record**-Objekt festgelegt werden. Die Dateien und Verzeichnisse, auf die über das **Connection**-Objekt zugegriffen werden kann, legen den *Kontext* fest, in dem **Record**-Vorgänge auftreten können.

Die Methoden der Datenänderung und Navigation des **Record** -Objekts akzeptieren auch eine relative URL, die eine Ressource mithilfe einer absoluten URL oder des **Connection** -Objektkontexts als Startpunkt suchen.

> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).



Jedem **Record** -Objekt ist ein **Connection** -Objekt zugeordnet. Aus diesem Grund können Vorgänge des **Record** -Objekts als Teil einer Transaktion verwendet werden, indem Transaktionsmethoden des **Connection** -Objekts aufgerufen werden.

Das **Record** -Objekt unterstützt keine ADO-Ereignisse und antwortet daher nicht auf Benachrichtigungen.

Mit den Methoden und Eigenschaften eines **Record** -Objekts können Sie die folgenden Aufgaben ausführen:

  - Festlegen oder Zurückgeben des zugeordneten **Connection** -Objekts mit der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft.

  - Angeben der Zugriffsberechtigungen mit der [Mode](mode-property-ado.md)-Eigenschaft.

  - Zurückgeben der URL des Verzeichnisses, falls vorhanden, das die vom **Record** -Objekt dargestellte Ressource enthält, mit der [ParentURL](parenturl-property-ado.md)-Eigenschaft.

  - Angeben der absoluten URL, der relativen URL oder des **Recordset** -Objekts, von dem das **Record** -Objekt stammt, mit der [Source](source-property-ado-record.md)-Eigenschaft.

  - Angeben des aktuellen Status des **Record**-Objekts mit der [State](state-property-ado.md)-Eigenschaft.

  - Angeben des Typs des **Record**-Objekts – *einfach*, *Auflistung* oder *strukturiertes Dokument* – mit der [RecordType](recordtype-property-ado.md)-Eigenschaft.

  - Anhalten der Ausführung eines asynchronen Vorgangs mit der [Cancel](cancel-method-ado.md)-Methode.

  - Entkoppeln des **Record** -Objekts von einer Datenquelle mit der [Close](close-method-ado.md)-Methode.

  - Kopieren der Datei oder des Verzeichnisse, das von einem **Record** -Objekt dargestellt wird, an eine andere Position mit der [CopyRecord](copyrecord-method-ado.md)-Methode.

  - Löschen der Datei oder des Verzeichnisses und seiner Unterverzeichnisse, die von einem **Record** -Objekt dargestellt werden, mit der [DeleteRecord](deleterecord-method-ado.md)-Methode.

  - Öffnen eines **Recordset** -Objekts mit Zeilen, die die Unterverzeichnisse und Dateien der vom **Record** -Objekt dargestellten Entität repräsentieren, mit der [GetChildren](getchildren-method-ado.md)-Methode.

  - Verschieben (Umbenennen) der von einem **Record** -Objekt dargestellten Datei oder des Verzeichnisses und seiner Unterverzeichnisse an einen anderen Speicherort mit der [MoveRecord](moverecord-method-ado.md)-Methode.

  - Zuordnen des **Record** -Objekts zu einer vorhandenen Datenquelle oder Erstellen einer neuen Datei oder eines neuen Verzeichnisses mit der [Open](open-method-ado-record.md)-Methode.

