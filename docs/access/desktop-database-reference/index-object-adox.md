---
title: Index-Objekt (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5bc2eeaf4d26c957abb67780fe2f5d0df8f73049
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026176"
---
# <a name="index-object-adox"></a>Index-Objekt (ADOX)

**Betrifft**: Access 2013, Office 2013

Stellt einen Index aus einer Datenbanktabelle dar.

## <a name="remarks"></a>Hinweise

Mit dem folgenden Code wird ein neues **Index** -Objekt erstellt:

`Dim obj As New Index`

Die Eigenschaften und Auflistungen eines **Index** -Objekts ermöglichen Folgendes:

- Identifizieren des Indexes, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

- Zugreifen auf die Datenbankspalten des Indexes, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.

- Angeben, ob die Indexschlüssel eindeutig sein müssen, indem Sie die [Unique](unique-property-adox.md)-Eigenschaft verwenden.

- Angeben, ob der Index den Primärschlüssel einer Tabelle darstellt, indem Sie die [PrimaryKey](primarykey-property-adox.md)-Eigenschaft verwenden.

- Angeben, ob Datensätze mit Nullwerten im Indexfeld über Indexeinträge verfügen, indem Sie die [IndexNulls](indexnulls-property-adox.md)-Eigenschaft verwenden.

- Angeben, ob der Index gruppiert ist, indem Sie die [Clustered](clustered-property-adox.md)-Eigenschaft verwenden.

- Zugreifen auf anbieterspezifische Indexeigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.


> [!NOTE]
> [!HINWEIS] Es tritt ein Fehler auf, wenn ein [Column](column-object-adox.md)-Objekt an die **Columns** -Auflistung eines **Index** -Objekts angefügt wird und das **Column** -Objekt nicht in einem [Table](table-object-adox.md)-Objekt vorhanden ist, das bereits an die [Tables](tables-collection-adox.md)-Auflistung angefügt wurde.

Möglicherweise werden nicht alle Eigenschaften für **Index** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Index** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.

Beim Erstellen von **Index** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.

