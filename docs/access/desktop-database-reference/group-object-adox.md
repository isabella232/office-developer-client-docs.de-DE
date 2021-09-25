---
title: Group-Objekt (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3d131d89dbcc67f244010fc0cee86bad30f78c2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606695"
---
# <a name="group-object-adox"></a>Group-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Stellt ein Gruppenkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.

## <a name="remarks"></a>HinwBemerkungeneise

Die [Groups](groups-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.

Die Eigenschaften, Auflistungen und Methoden eines **Group** -Objekts ermöglichen Folgendes:

  - Identifizieren der Gruppe, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Bestimmen, ob eine Gruppe Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.

  - Zugreifen auf die Benutzerkonten, die Mitgliedschaften in der Gruppe haben, indem Sie die [Users](users-collection-adox.md)-Auflistung verwenden.

  - Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.

