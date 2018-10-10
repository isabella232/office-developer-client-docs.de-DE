---
title: Group-Objekt (ADOX)
TOCTitle: Group Object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21caab66c16c4ca9f77c49f33bf99f4df7be79c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475051"
---
# <a name="group-object-adox"></a>Group-Objekt (ADOX)


**Betrifft**: Access 2013 | Office 2013

Stellt ein Gruppenkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.

## <a name="remarks"></a>Hinweise

Die [Groups](groups-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.

Die Eigenschaften, Auflistungen und Methoden eines **Group** -Objekts ermöglichen Folgendes:

  - Identifizieren der Gruppe, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Bestimmen, ob eine Gruppe Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.

  - Zugreifen auf die Benutzerkonten, die Mitgliedschaften in der Gruppe haben, indem Sie die [Users](users-collection-adox.md)-Auflistung verwenden.

  - Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.

