---
title: Recordset.BatchCollisions Property (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9b9b867b54061f574741a7da2817988994ab968f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473854"
---
# <a name="recordsetbatchcollisions-property-dao"></a>Recordset.BatchCollisions Property (DAO)


**Betrifft**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . BatchCollisions

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält ein Array der Textmarken für Zeilen, die beim letzten Versuch eines **[Update](recordset-update-method-dao.md)** -Batchaufrufs Konflikte verursacht haben. Die **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** -Eigenschaft gibt die Anzahl von Elementen im Array an.

Wenn Sie die **[Bookmark](recordset-object-dao.md)** -Eigenschaft des aktiven **[Recordset](recordset-bookmark-property-dao.md)** -Objekts auf Textmarkenwerte im **BatchCollisions**-Array festlegen, können Sie zu jedem Datensatz wechseln, bei dem die letzte Batchaktualisierungsoperation nicht abgeschlossen werden konnte.

Nachdem die Konflikte verursachenden Datensätze korrigiert wurden, kann erneut eine Update-Methode im Batchmodus aufgerufen werden. An dieser Stelle versucht DAO eine weitere Batchaktualisierung, und die BatchCollisions-Eigenschaft gibt erneut die Datensätze zurück, bei denen der zweite Versuch fehlschlug. Datensätze, bei denen der vorhergehende Versuch erfolgreich war, werden nicht erneut gesendet, da deren RecordStatus-Eigenschaft auf dbRecordUnmodified festgelegt ist. Dieser Prozess kann fortgesetzt werden, bis Sie die Aktualisierung abbrechen und das Resultset schließen.

Dieses Array wird bei jedem Ausführen einer **Update**-Methode im Batchmodus neu erstellt.

