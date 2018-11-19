---
title: Catalog-Objekt (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d680c89f7188dafd216edf62bd07c80fa924a119
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026239"
---
# <a name="catalog-object-adox"></a>Catalog-Objekt (ADOX)


**Betrifft**: Access 2013, Office 2013

Enthält Auflistungen ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) und [Procedures](procedures-collection-adox.md)), die den Schemakatalog einer Datenquelle beschreiben.

## <a name="remarks"></a>Hinweise

Sie können das **Catalog** -Objekt ändern, indem Sie Objekte hinzufügen oder entfernen oder vorhandene Objekte bearbeiten. Einige Anbieter unterstützen möglicherweise nicht alle **Catalog** -Objekte oder sie unterstützen nur das Anzeigen von Schemainformationen.

Die Eigenschaften und Methoden eines **Catalog** -Objekts ermöglichen Folgendes:

- Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Objekt oder eine gültige Verbindungszeichenfolge festlegen.

- Erstellen eines neuen Katalogs, indem Sie die [Create](create-method-adox.md)-Methode verwenden.

- Bestimmen der Besitzer von Objekten in einem **Catalog** -Objekt, indem Sie die Methoden [GetObjectOwner](getobjectowner-method-adox.md) und [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) verwenden.

