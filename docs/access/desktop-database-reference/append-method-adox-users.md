---
title: Append-Methode (ADOX Users)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c09076444c6830b114db27fe4adfa0104718b80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559003"
---
# <a name="append-method-adox-users"></a>Append-Methode (ADOX Users)

**Gilt für**: Access 2013, Office 2013

Fügt der [Users](user-object-adox.md)-Auflistung ein neues [User](users-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Benutzer*. Benutzer \[ anhängen ,*Kennwort*\]

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*User* |Ein **Variant** -Wert, der das anzufügende **User** -Objekt enthält oder den Namen des zu erstellenden und anzufügenden Benutzers.|
|*Password* |Optional. Ein **String**-Wert, der das Kennwort für den Benutzer enthält. Der *Password*-Parameter entspricht dem Wert, der durch die [ChangePassword](changepassword-method-adox.md)-Methode eines **User**-Objekts angegeben wird.|

## <a name="remarks"></a>HinwBemerkungeneise

Die **Users** Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Benutzer des Katalogs dar. Die **Users** -Auflistung für ein [Group](group-object-adox.md)-Objekt stellt nur die Benutzer dar, die Elemente dieser bestimmten Gruppe sind.

Wenn der Anbieter das Erstellen von Benutzern nicht unterstützt, tritt ein Fehler auf.

> [!NOTE]
> [!HINWEIS] Bevor ein **User** -Objekt an die **Users** -Auflistung eines **Group** -Objekts angefügt wird, muss ein **User** -Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Users** -Auflistung des **Catalog** -Objekts vorhanden sein.


