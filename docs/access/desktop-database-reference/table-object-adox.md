---
title: Table-Objekt (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4bcf3c62cd7c357d3fa9ba9050f5a26bc134d009
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585221"
---
# <a name="table-object-adox"></a>Table-Objekt (ADOX)

**Gilt für**: Access 2013, Office 2013

Stellt eine Datenbanktabelle dar, einschließlich Spalten, Indizes und Schlüsseln.

## <a name="remarks"></a>HinwBemerkungeneise

Mit dem folgenden Code wird ein neues **Table**-Objekt erstellt:

`Dim obj As New Table`

Die Eigenschaften und Auflistungen eines **Table**-Objekts ermöglichen Folgendes:

- Identifizieren der Tabelle, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

- Bestimmen des Tabellentyps, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)-Eigenschaft verwenden.

- Zugreifen auf die Datenbankspalten der Tabelle, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.

- Zugreifen auf die Indizes der Tabelle, indem Sie die [Indexes](indexes-collection-adox.md)-Auflistung verwenden.

- Zugreifen auf die Schlüssel der Tabelle, indem Sie die [Keys](keys-collection-adox.md)-Auflistung verwenden.

- Angeben des [Catalog](catalog-object-adox.md)-Objekts, das im Besitz der Tabelle ist, indem Sie die [ParentCatalog](parentcatalog-property-adox.md)-Eigenschaft verwenden.

- Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.

- Zugreifen auf anbieterspezifische Tabelleneigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.


> [!NOTE]
> [!HINWEIS] Möglicherweise werden nicht alle Eigenschaften für **Table** -Objekte von Ihrem Datenprovider unterstützt. Wenn Sie einen Wert für eine Eigenschaft festlegen, die nicht vom Provider unterstützt wird, tritt ein Fehler auf. Bei neuen **Table** -Objekten tritt der Fehler auf, wenn das Objekt der Auflistung hinzugefügt wird. Bei vorhandenen Objekten tritt der Fehler auf, wenn die Eigenschaft festgelegt wird.

Beim Erstellen von **Table** -Objekten gewährleistet das Vorhandensein eines entsprechenden Standardwerts für eine optionale Eigenschaft nicht, dass diese Eigenschaft vom Provider unterstützt wird. Weitere Informationen zu den vom Provider unterstützten Eigenschaften finden Sie in der Providerdokumentation.

