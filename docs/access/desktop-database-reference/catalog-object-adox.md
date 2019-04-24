---
title: Catalog-Objekt (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8cc0237d1419c3aba818d54811f1dbdeeaa441c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296570"
---
# <a name="catalog-object-adox"></a>Catalog-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Enthält Auflistungen ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) und [Procedures](procedures-collection-adox.md)), die den Schemakatalog einer Datenquelle beschreiben.

## <a name="remarks"></a>Bemerkungen

Sie können das **Catalog**-Objekt ändern, indem Sie Objekte hinzufügen oder entfernen oder vorhandene Objekte bearbeiten. Einige Anbieter unterstützen möglicherweise nicht alle **Catalog**-Objekte oder sie unterstützen nur das Anzeigen von Schemainformationen.

Die Eigenschaften und Methoden eines **Catalog** -Objekts ermöglichen Folgendes:

- Öffnen des Katalogs, indem Sie für die [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft ein [Connection](connection-object-ado.md)-ADO-Objekt oder eine gültige Verbindungszeichenfolge festlegen.

- Erstellen eines neuen Katalogs, indem Sie die [Create](create-method-adox.md)-Methode verwenden.

- Bestimmen der Besitzer von Objekten in einem **Catalog**-Objekt, indem Sie die Methoden [GetObjectOwner](getobjectowner-method-adox.md) und [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) verwenden.

