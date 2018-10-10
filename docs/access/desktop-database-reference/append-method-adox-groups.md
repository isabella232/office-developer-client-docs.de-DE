---
title: Append-Method (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475694"
---
# <a name="append-method-adox-groups"></a>Append-Method (ADOX Groups)


**Betrifft**: Access 2013 | Office 2013



Fügt der [Groups](group-object-adox.md)-Auflistung ein neues [Group](groups-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Gruppen*. Fügen Sie die*Gruppe*

## <a name="parameters"></a>Parameter

  - *Group*

  - Das anzufügende **Group** -Objekt oder der Name der zu erstellenden und anzufügenden Gruppe.

## <a name="remarks"></a>Hinweise

Die **Groups** -Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups** -Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.

Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.


> [!NOTE]
> <P>[!HINWEIS] Bevor ein <STRONG>Group</STRONG> -Objekt an die <STRONG>Groups</STRONG> -Auflistung eines <STRONG>User</STRONG> -Objekts angefügt wird, muss ein <STRONG>Group</STRONG> -Objekt mit demselben <A href="name-property-adox.md">Namen</A> wie das anzufügende Objekt bereits in der <STRONG>Groups</STRONG> -Auflistung des <STRONG>Catalog</STRONG> -Objekts vorhanden sein.</P>


