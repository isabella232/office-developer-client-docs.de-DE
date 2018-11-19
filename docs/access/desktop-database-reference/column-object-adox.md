---
title: Column-Objekt (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1b7ebd312727e1dc5071964cf1125d1c76bec4d
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026008"
---
# <a name="column-object-adox"></a>Column-Objekt (ADOX)


**Betrifft**: Access 2013, Office 2013

Stellt eine Spalte aus einer Tabelle, einem Index oder einem Schlüssel dar.

## <a name="remarks"></a>Hinweise

Mit dem folgenden Code wird ein neues **Column** -Objekt erstellt:

`Dim obj As New Column`

Die Eigenschaften und Auflistungen eines **Column** -Objekts ermöglichen Folgendes:

  - Identifizieren der Spalte, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Angeben des Datentyps für die Spalte, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)-Eigenschaft verwenden.

  - Bestimmen, ob die Spalte eine feste Länge hat oder ob sie Nullwerte enthalten kann, indem Sie die [Attributes](attributes-property-adox.md)-Eigenschaft verwenden.

  - Angeben der maximalen Spaltengröße, indem Sie die [DefinedSize](definedsize-property-adox.md)-Eigenschaft verwenden.

  - Für numerische Datenwerte: Angeben der Skalierung, indem Sie die [NumericScale](numericscale-property-adox.md)-Eigenschaft verwenden.

  - Für numerische Datenwerte: Angeben der höchsten Genauigkeit, indem Sie die [Precision](precision-property-adox.md)-Eigenschaft verwenden.

  - Angeben des [Catalog](catalog-object-adox.md)-Objekts, das im Besitz der Spalte ist, indem Sie die [ParentCatalog](parentcatalog-property-adox.md)-Eigenschaft verwenden.

  - Für Schlüsselspalten: Angeben des Namens der verwandten Spalte in der verwandten Tabelle, indem Sie die [RelatedColumn](relatedcolumn-property-adox.md)-Eigenschaft verwenden.

  - Für Indexspalten: Angeben, ob die Daten auf- oder absteigend sortiert werden, indem Sie die [SortOrder](sortorder-property-adox.md)-Eigenschaften verwenden.

  - Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.


> [!NOTE]
> [!HINWEIS] Möglicherweise werden nicht alle Eigenschaften für **Column** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Column** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.
> 
> Beim Erstellen von **Column** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.

