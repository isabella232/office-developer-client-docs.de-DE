---
title: Recordset2.UpdateOptions-Eigenschaft (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698666"
---
# <a name="recordset2updateoptions-property-dao"></a>Recordset2.UpdateOptions-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . UpdateOptions

*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn eine **[Update](recordset2-update-method-dao.md)** -Anweisung im Batchmodus ausgeführt wird, erstellen DAO und die Client-Batchcursorbibliothek eine Reihe von SQL UPDATE-Anweisungen, um die erforderlichen Änderungen auszuführen. Für jede Aktualisierung wird eine SQL WHERE-Klausel erstellt, um die Datensätze zu isolieren, die von der **[RecordStatus](recordset2-recordstatus-property-dao.md)** -Eigenschaft als geändert markiert wurden. Da einige Remoteserver Trigger oder andere Wege verwenden, um die referenzielle Integrität zu erzwingen, müssen häufig die zu aktualisierenden Felder auf die Felder beschränkt werden, die von der Änderung betroffen sind. 

Hierzu legen Sie die **UpdateOptions**-Eigenschaft auf eine der Konstanten **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** oder **dbCriteriaTimeStamp** fest. Auf diese Weise wird nur der absolut notwendige Triggercode ausgeführt. Als Ergebnis wird der Aktualisierungsvorgang schneller und mit weniger potenziellen Fehlern ausgeführt.

Sie können auch die Konstanten **dbCriteriaDeleteInsert** und **dbCriteriaUpdate** verketten, um festzustellen, ob für jede Aktualisierung eine Gruppe von SQL DELETE- und INSERT-Anweisungen oder eine SQL UPDATE-Anweisung verwendet werden sollen, wenn Änderungen in einem Batch an den Server zurückgesendet werden. Im ersten Fall sind zwei separate Vorgänge erforderlich, um den Datensatz zu aktualisieren. In einigen Fällen, v. a. wenn das Remotesystem DELETE-, INSERT- und UPDATE-Trigger implementiert, kann die Wahl der richtigen **UpdateOptions**-Eigenschaft erheblichen Einfluss auf die Leistung haben.

Wenn Sie keine Konstanten angeben, werden **dbCriteriaUpdate** und **dbCriteriaKey** verwendet.

Neu hinzugefügte Datensätze generieren immer INSERT-Anweisungen, und gelöschte Datensätze generieren immer DELETE-Anweisungen, sodass diese Eigenschaft nur angibt, wie die Cursorbibliothek geänderte Datensätze aktualisiert.

