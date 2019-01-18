---
title: Recordset.BatchCollisions-Eigenschaft (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f60567ac170a0ecde2d4bd46589d2308b7788f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700372"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Recordset.BatchCollisions-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisions

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält ein Array der Textmarken für Zeilen, die beim letzten Versuch eines **[Update](recordset-update-method-dao.md)** -Batchaufrufs Konflikte verursacht haben. Die **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl von Elementen im Array an.

Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte Batchaktualisierungsoperation nicht abgeschlossen werden konnte.

Nachdem die Konflikte verursachenden Datensätze korrigiert wurden, kann erneut eine Update-Methode im Batchmodus aufgerufen werden. An dieser Stelle versucht DAO eine weitere Batchaktualisierung, und die BatchCollisions-Eigenschaft gibt erneut die Datensätze zurück, bei denen der zweite Versuch fehlschlug. Datensätze, bei denen der vorhergehende Versuch erfolgreich war, werden nicht erneut gesendet, da deren RecordStatus-Eigenschaft auf dbRecordUnmodified festgelegt ist. Dieser Prozess kann fortgesetzt werden, bis Sie die Aktualisierung abbrechen und das Resultset schließen.

Dieses Array wird bei jedem Ausführen einer **Update**-Methode im Batchmodus neu erstellt.

