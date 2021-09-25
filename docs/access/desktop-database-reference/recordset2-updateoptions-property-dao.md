---
title: Recordset2.UpdateOptions-Eigenschaft (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 69e867eae41c0189302d18ff833db2e137596d2c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572774"
---
# <a name="recordset2updateoptions-property-dao"></a>Recordset2.UpdateOptions-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . UpdateOptions

*Ausdruck* Eine Variable, die ein **Recordset2-Objekt** darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine **[Update](recordset2-update-method-dao.md)** -Anweisung im Batchmodus ausgeführt wird, erstellen DAO und die Client-Batchcursorbibliothek eine Reihe von SQL UPDATE-Anweisungen, um die erforderlichen Änderungen auszuführen. Für jede Aktualisierung wird eine SQL WHERE-Klausel erstellt, um die Datensätze zu isolieren, die von der **[RecordStatus](recordset2-recordstatus-property-dao.md)** -Eigenschaft als geändert markiert wurden. Da einige Remoteserver Trigger oder andere Wege verwenden, um die referenzielle Integrität zu erzwingen, müssen häufig die zu aktualisierenden Felder auf die Felder beschränkt werden, die von der Änderung betroffen sind. 

Hierzu legen Sie die **UpdateOptions**-Eigenschaft auf eine der Konstanten **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** oder **dbCriteriaTimeStamp** fest. Auf diese Weise wird nur der absolut notwendige Triggercode ausgeführt. Als Ergebnis wird der Aktualisierungsvorgang schneller und mit weniger potenziellen Fehlern ausgeführt.

Sie können auch die Konstanten **dbCriteriaDeleteInsert** und **dbCriteriaUpdate** verketten, um festzustellen, ob für jede Aktualisierung eine Gruppe von SQL DELETE- und INSERT-Anweisungen oder eine SQL UPDATE-Anweisung verwendet werden sollen, wenn Änderungen in einem Batch an den Server zurückgesendet werden. Im ersten Fall sind zwei separate Vorgänge erforderlich, um den Datensatz zu aktualisieren. In einigen Fällen, v. a. wenn das Remotesystem DELETE-, INSERT- und UPDATE-Trigger implementiert, kann die Wahl der richtigen **UpdateOptions**-Eigenschaft erheblichen Einfluss auf die Leistung haben.

Wenn Sie keine Konstanten angeben, werden **dbCriteriaUpdate** und **dbCriteriaKey** verwendet.

Neu hinzugefügte Datensätze generieren immer INSERT-Anweisungen, und gelöschte Datensätze generieren immer DELETE-Anweisungen, sodass diese Eigenschaft nur angibt, wie die Cursorbibliothek geänderte Datensätze aktualisiert.

