---
title: Recordset.MoveFirst-Methode (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b09723b816525ac538de54c3a85df53260496959
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585452"
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

Wenn sich Recordset auf ein **Recordset** vom Typ Tabelle bezieht (nur Microsoft Access-Arbeitsbereiche), folgt die Bewegung dem aktuellen Index. Sie können den aktuellen Index mit der Eigenschaft **Index** festlegen. Wenn Sie den aktuellen Index nicht festlegen, ist die Reihenfolge der zurückgegebenen Datensätze undefiniert.

Die Methoden **MoveFirst**, **MoveLast** und **MovePrevious** können für ein **Recordset**-Objekt vom Typ "Forward-only" nicht verwendet werden.

Um die Position des aktuellen Datensatzes in einem **Recordset**-Objekt um eine bestimmte Anzahl von Datensätzen nach vorne oder hinten zu verschieben, verwenden Sie die **Move**-Methode.

