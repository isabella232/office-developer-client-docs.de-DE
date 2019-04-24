---
title: Append-Methode (ADOX Users)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297067"
---
# <a name="append-method-adox-users"></a>Append-Methode (ADOX Users)

**Gilt für**: Access 2013, Office 2013

Fügt der [Users](user-object-adox.md)-Auflistung ein neues [User](users-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Benutzer*. Anhängen von*Benutzer*\[,*Kennwort*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*User* |Ein **Variant** -Wert, der das anzufügende **User** -Objekt enthält oder den Namen des zu erstellenden und anzufügenden Benutzers.|
|*Password* |Optional. Ein **String**-Wert, der das Kennwort für den Benutzer enthält. Der *Password*-Parameter entspricht dem Wert, der durch die [ChangePassword](changepassword-method-adox.md)-Methode eines **User**-Objekts angegeben wird.|

## <a name="remarks"></a>Bemerkungen

Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.

Wenn der Anbieter das Erstellen von Benutzern nicht unterstützt, tritt ein Fehler auf.

> [!NOTE]
> [!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.


