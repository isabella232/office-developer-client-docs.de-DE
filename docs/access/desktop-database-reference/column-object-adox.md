---
title: Column-Objekt (ADOX)
TOCTitle: Column Object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be5af50dd17934ece6ae3a00242a86e691ff337e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474978"
---
# <a name="column-object-adox"></a>Column-Objekt (ADOX)


**Betrifft**: Access 2013 | Office 2013

Stellt eine Spalte aus einer Tabelle, einem Index oder einem Schlüssel dar.

## <a name="remarks"></a>Hinweise

Mit dem folgenden Code wird ein neues **Column** -Objekt erstellt:

`Dim obj As New Column`

Die Eigenschaften und Auflistungen eines **Column** -Objekts ermöglichen Folgendes:

  - Identifizieren der Spalte, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Angeben des Datentyps für die Spalte, indem Sie die [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))-Eigenschaft verwenden.

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

