---
title: Groups-Auflistung (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6700e70a65499ef1c1c89dbcc50ccd5a23d50e2a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602486"
---
# <a name="groups-collection-adox"></a>Groups-Auflistung (ADOX)

**Gilt für**: Access 2013, Office 2013

Enthält alle gespeicherten [Group](group-object-adox.md)-Objekte eines Katalogs oder Benutzers.

## <a name="remarks"></a>HinwBemerkungeneise

Die **Groups**-Auflistung eines [Catalog](catalog-object-adox.md)-Objekts stellt alle Gruppenkonten des Katalogs dar. Die **Groups**-Auflistung für ein [User](user-object-adox.md)-Objekt stellt lediglich die Gruppe dar, zu der der Benutzer gehört.

Die [Append](append-method-adox-groups.md)-Methode für eine **Groups** -Auflistung wird nur für ADOX bereitgestellt. Sie haben folgende Möglichkeiten:

- Hinzufügen einer neuen Sicherheitsgruppe zur Auflistung, indem Sie die **Append** -Methode verwenden.

Die verbleibenden Eigenschaften und Methoden sind Standardbestandteile von ADO-Auflistungen. Sie haben folgende Möglichkeiten:

- Zugreifen auf eine Gruppe in der Auflistung, indem Sie die [Item](item-property-ado.md)-Eigenschaft verwenden.

- Zurückgeben der Anzahl der Gruppen, die in der Auflistung vorhanden sind, indem Sie die [Count](count-property-ado.md)-Eigenschaft verwenden.

- Entfernen einer Gruppe aus der Auflistung, indem Sie die [Delete](delete-method-adox-collections.md)-Methode verwenden.

- Aktualisieren der Objekte in der Auflistung entsprechend dem aktuellen Datenbankschema, indem Sie die [Refresh](refresh-method-ado.md)-Methode verwenden.

> [!NOTE]
> Bevor ein **Group**-Objekt an die **Groups**-Auflistung eines **User**-Objekts angefügt wird, muss ein **Group**-Objekt mit demselben [Namen](name-property-adox.md) wie das anzufügende Objekt bereits in der **Groups**-Auflistung des **Catalog**-Objekts vorhanden sein.


