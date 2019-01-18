---
title: Recordset2.BatchCollisions-Eigenschaft (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699758"
---
# <a name="recordset2batchcollisions-property-dao"></a>Recordset2.BatchCollisions-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisions

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält ein Array von Lesezeichen für Zeilen, die beim letzten Versuch einer Batchaktualisierung (Aufruf von **[Update](recordset2-update-method-dao.md)** ) einen Konflikt verursacht haben. Die **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl der Elemente im Array an.

Wenn Sie die [**Bookmark**](recordset2-bookmark-property-dao.md) -Eigenschaft des **Recordset**-Objekts festlegen, um Werte im **BatchCollisions**-Array mit einem Lesezeichen zu versehen, können Sie zu jedem Datensatz navigieren, der beim letzten Batchaktualisierungsvorgang nicht verarbeitet werden konnte.

Nachdem die Konflikte verursachenden Datensätze korrigiert wurden, kann erneut eine Update-Methode im Batchmodus aufgerufen werden. An dieser Stelle versucht DAO eine weitere Batchaktualisierung, und die BatchCollisions-Eigenschaft gibt erneut die Datensätze zurück, bei denen der zweite Versuch fehlschlug. Datensätze, bei denen der vorhergehende Versuch erfolgreich war, werden nicht erneut gesendet, da deren RecordStatus-Eigenschaft auf dbRecordUnmodified festgelegt ist. Dieser Prozess kann fortgesetzt werden, bis Sie die Aktualisierung abbrechen und das Resultset schließen.

Dieses Array wird bei jedem Ausführen einer **Update**-Methode im Batchmodus neu erstellt.

