---
title: Recordset.MoveFirst-Methode (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300238"
---
# <a name="recordsetmovefirst-method-dao"></a>Recordset.MoveFirst-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Wechselt zum ersten Datensatz in einem angegebenen **Recordset**-Objekt und macht diesen zum aktuellen Datensatz.

## <a name="syntax"></a>Syntax

*Ausdruck* .MoveFirst

*Ausdruck* Eine Variable, die ein **Recordset**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Move**-Methoden, um von einem Datensatz zum nächsten zu wechseln, ohne eine Bedingung anzuwenden.

Wenn Sie den aktuellen Datensatz bearbeiten, sollten Sie die Änderungen mit der **Update**-Methode speichern, bevor Sie zu einem anderen Datensatz wechseln. Ohne diese Aktualisierung gehen die Änderungen beim Wechseln zwischen Datensätzen ohne Warnung verloren.

Beim Öffnen eines **Recordset**-Objekts ist der erste Datensatz aktuell, und die **BOF**-Eigenschaft ist auf **False** festgelegt. Wenn **Recordset** keine Datensätze enthält, ist die **BOF**-Eigenschaft auf **True** festgelegt, und es ist kein aktueller Datensatz vorhanden.

Wenn der erste oder letzte Datensatz bei Verwendung von **MoveFirst** oder **MoveLast** bereits aktuell ist, ändert sich der aktuelle Datensatz nicht.

Wenn Recordset sich auf ein **Recordset** vom Typ "Tabelle" bezieht (nur Microsoft Access-Arbeitsbereiche), folgt die Bewegung dem aktuellen Index. You can set the current index by using the **Index** property. Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze nicht definiert.

Die Methoden **MoveFirst**, **MoveLast** und **MovePrevious** können für ein **Recordset**-Objekt vom Typ "Forward-only" nicht verwendet werden.

Um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen nach vorne oder hinten zu verschieben, verwenden Sie die **Move**-Methode.

