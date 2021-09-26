---
title: Append-Methode (ADOX Groups)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8e8aab9b70fc418c471599885e4061bfd7762176
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607360"
---
# <a name="append-method-adox-groups"></a>Append-Methode (ADOX Groups)

**Gilt für**: Access 2013, Office 2013

Fügt der [Groups](group-object-adox.md)-Auflistung ein neues [Group](groups-collection-adox.md)-Objekt hinzu.

## <a name="syntax"></a>Syntax

*Gruppen*. *Append-Gruppe*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Group* |Das anzufügende **Group** -Objekt oder der Name der zu erstellenden und anzufügenden Gruppe.|

## <a name="remarks"></a>HinwBemerkungeneise

Die **Groups**-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups**-Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.

Wenn der Anbieter das Erstellen von Gruppen nicht unterstützt, tritt ein Fehler auf.

> [!NOTE]
> Bevor ein **Group**-Objekt an die **Groups**-Auflistung eines **User**-Objekts angefügt wird, muss ein **Group**-Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Groups**-Auflistung des **Catalog**-Objekts vorhanden sein.


