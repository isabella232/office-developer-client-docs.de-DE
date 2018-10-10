---
title: Append-Methode (ADOX Users)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8bce151e800b58e9c99c6dd6591114c53208a5c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473447"
---
# <a name="append-method-adox-users"></a>Append-Methode (ADOX Users)


**Betrifft**: Access 2013 | Office 2013


Fügt der [Users](user-object-adox.md)-Auflistung ein neues [User](users-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Benutzer*. Fügen Sie*Benutzer*\[,*Kennwort*\]

## <a name="parameters"></a>Parameters

  - *User*

  - Ein **Variant** -Wert, der das anzufügende **User** -Objekt enthält oder den Namen des zu erstellenden und anzufügenden Benutzers.

  - *Password*

  - Optional. Ein **String** -Wert, der das Kennwort für den Benutzer enthält. Der Parameter *Password* entspricht dem Wert, der durch die [ChangePassword](changepassword-method-adox.md) -Methode des **User** -Objekt angegeben.

## <a name="remarks"></a>Hinweise

Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.

Wenn der Anbieter das Erstellen von Benutzern nicht unterstützt, tritt ein Fehler auf.


> [!NOTE]
> <P>[!HINWEIS] Bevor ein <STRONG>User</STRONG> -Objekt an die <STRONG>Users</STRONG> -Auflistung eines <STRONG>Group</STRONG> -Objekts angefügt wird, muss ein <STRONG>User</STRONG> -Objekt mit demselben <A href="name-property-adox.md">Namen</A> wie das anzufügende Objekt bereits in der <STRONG>Users</STRONG> -Auflistung des <STRONG>Catalog</STRONG> -Objekts vorhanden sein.</P>


