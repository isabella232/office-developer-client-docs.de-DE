---
title: User-Objekt (ADOX – Access-Desktopdatenbankreferenz)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8bd62da5b813985c725703cca80a75aabbac73fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593355"
---
# <a name="user-object-adox"></a>User-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Stellt ein Benutzerkonto dar, das über Zugriffsberechtigungen in einer gesicherten Datenbank verfügt.

## <a name="remarks"></a>HinwBemerkungeneise

Die [Users](users-collection-adox.md)-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users**-Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dieser Gruppe dar.

Die Eigenschaften, Auflistungen und Methoden eines **User** -Objekts ermöglichen Folgendes:

  - Identifizieren des Benutzers, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Ändern des Kennworts eines Benutzers, indem Sie die [ChangePassword](changepassword-method-adox.md)-Methode verwenden.

  - Bestimmen, ob ein Benutzer Lese-, Schreib- oder Löschberechtigungen hat, indem Sie die Methoden [GetPermissions](getpermissions-method-adox.md) und [SetPermissions](setpermissions-method-adox.md) verwenden.

  - Zugreifen auf die Gruppen, denen ein Benutzer angehört, indem Sie die [Groups](groups-collection-adox.md)-Auflistung verwenden.

  - Zugreifen auf anbieterspezifische Eigenschaften mit der [Properties](properties-collection-ado.md)-Auflistung.

