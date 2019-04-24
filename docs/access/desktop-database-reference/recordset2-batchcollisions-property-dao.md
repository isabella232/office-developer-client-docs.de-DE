---
title: Recordset2. BatchCollisions-Eigenschaft (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ea75da06c0db4eeb4e846bacfddc9f125c03fc84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307490"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2. BatchCollisions-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisions

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält ein Array von Lesezeichen für Zeilen, die beim letzten Versuch einer Batchaktualisierung (Aufruf von **[Update](recordset2-update-method-dao.md)** ) einen Konflikt verursacht haben. Die **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl der Elemente im Array an.

Wenn Sie die [**Bookmark**](recordset2-bookmark-property-dao.md) -Eigenschaft des **Recordset**-Objekts festlegen, um Werte im **BatchCollisions**-Array mit einem Lesezeichen zu versehen, können Sie zu jedem Datensatz navigieren, der beim letzten Batchaktualisierungsvorgang nicht verarbeitet werden konnte.

After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.

Dieses Array wird bei jeder Ausführung einer **Update**-Methode im Batchmodus neu erstellt.

