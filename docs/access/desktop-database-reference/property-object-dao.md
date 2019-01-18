---
title: Property-Objekt (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718819"
---
# <a name="property-object-dao"></a>Property-Objekt (DAO)

**Betrifft**: Access 2013, Office 2013

Ein **Property**-Objekt stellt eine integrierte oder benutzerdefinierte Eigenschaft eines DAO-Objekts dar.

## <a name="remarks"></a>Bemerkungen

Alle DAO-Objekte, außer den Objekten **Connection** und **Error**, enthalten eine **Properties**-Auflistung mit **Property**-Objekten, die den integrierten Eigenschaften dieses DAO-Objekts entsprechen. Der Benutzer kann außerdem **Property**-Objekte definieren und sie der **Properties**-Auflistung eines DAO-Objekts anfügen. Diese **Property**-Objekte (die häufig lediglich "Eigenschaften" genannt werden) kennzeichnen die betreffende Objektinstanz eindeutig.

Sie können für die folgenden Objekte benutzerdefinierte Eigenschaften erstellen:

- **Database**-, **Index**-, **QueryDef**- und **TableDef**-Objekte

- **Field**-Objekte in **Fields**-Auflistungen von **QueryDef**- und **TableDef**-Objekten

Um eine benutzerdefinierte Eigenschaft hinzuzufügen, erstellen Sie mit der **CreateProperty**-Methode ein **Property**-Objekt mit einer eindeutigen Einstellung der **Name**-Eigenschaft. Legen Sie die Eigenschaften **Type** und **Value** des neuen **Property**-Objekts fest, und fügen Sie es dann der **Properties**-Auflistung des entsprechenden Objekts an. Das Objekt, dem Sie die benutzerdefinierte Eigenschaft hinzufügen, muss bereits Bestandteil einer Auflistung sein. Wenn auf ein benutzerdefiniertes **Property**-Objekt verwiesen wird, das noch keiner **Properties**-Auflistung angefügt ist, tritt ein Fehler auf. Ein Fehler tritt auch auf, wenn ein benutzerdefiniertes **Property**-Objekt einer **Properties**-Auflistung angefügt wird, die bereits ein **Property**-Objekt desselben Namens enthält.

Sie können benutzerdefinierte Eigenschaften aus der **Properties**-Auflistung entfernen, integrierte Eigenschaften können jedoch nicht gelöscht werden.

> [!NOTE]
> [!HINWEIS] Ein benutzerdefiniertes **Property**-Objekt ist nur einer bestimmten Objektinstanz zugeordnet. Die Eigenschaft ist nicht für alle Objektinstanzen des ausgewählten Typs definiert.

Mithilfe der **Properties**-Auflistung eines Objekts können Sie dessen integrierte und benutzerdefinierte Eigenschaften auflisten. Zu diesem Zweck müssen Sie nicht genau wissen, welche Eigenschaften vorhanden sind oder mit welchen Merkmalen (**Name**- und **Type**-Eigenschaft) sie bearbeitet werden. Ein Fehler tritt jedoch auf, wenn Sie eine lesegeschützte Eigenschaft zu lesen versuchen (z. B. die **Password**-Eigenschaft eines **Workspace**-Objekts), oder wenn Sie versuchen, eine Eigenschaft in einem ungeeigneten Kontext zu lesen oder zu schreiben (z. B. die Einstellung der **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts).

Das **Property**-Objekt besitzt auch vier integrierte Eigenschaften:

- Die **Name**-Eigenschaft mit einem **String**-Wert, der die Eigenschaft eindeutig identifiziert.

- Die **Type**-Eigenschaft mit einem **Integer**-Wert, der den Datentyp der Eigenschaft angibt.

- Die **Value**-Eigenschaft mit einem **Variant**-Wert, der die Einstellung der Eigenschaft enthält.

- Die **Inherited**-Eigenschaft mit einem **Boolean**-Wert, der angibt, ob die Eigenschaft von einem anderen Objekt vererbt wurde. Ein **Field**-Objekt in einer **Fields**-Auflistung eines **Recordset**-Objekts kann z. B. Eigenschaften des zugrunde liegenden **TableDef**- oder **QueryDef**-Objekts erben.

Wenn Sie auf ein integriertes **Property**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

- * Objekt ***. Eigenschaften**(0)

- Objekt ****. Eigenschaften**("* Name *")

- Objekt ****. Eigenschaften**\!* Namen *\]

Bei einer integrierten Eigenschaft können Sie auch diese Syntax verwenden:

- - *Objekt*. *Name*

> [!NOTE]
> Für eine benutzerdefinierte Eigenschaft müssen Sie die vollständige *Objekt ***verwenden. Eigenschaften**("* Name *") Syntax.

Sie können mit denselben Syntaxformen auf die **Value**-Eigenschaft eines **Property**-Objekts verweisen. Der Kontext des Verweises entscheidet, ob Sie sich auf das **Property**-Objekt selbst oder auf die **Value**-Eigenschaft des **Property**-Objekts beziehen.

