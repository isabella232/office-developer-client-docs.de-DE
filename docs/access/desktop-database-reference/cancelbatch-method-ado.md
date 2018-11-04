---
title: CancelBatch-Methode (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88bf83cad220056d9ee21f300e5543030e5d18cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950078"
---
# <a name="cancelbatch-method-ado"></a>CancelBatch-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Eine ausstehende Batchaktualisierung wird abgebrochen.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. CancelBatch *AffectRecords*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*AffectRecords* |Optional. Ein [AffectEnum](affectenum.md)-Wert, durch den angegeben wird, auf wie viele Datensätze sich die **CancelBatch** -Methode auswirkt. |

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CancelBatch** -Methode, um alle ausstehenden Aktualisierungen in einem [Recordset](recordset-object-ado.md) im Batchaktualisierungsmodus abzubrechen. Wenn sich das **Recordset** im Modus für sofortige Aktualisierungen befindet, wird durch Aufrufen von **CancelBatch** ohne **adAffectCurrent** ein Fehler generiert.

Wenn Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie **CancelBatch** aufrufen, wird von ADO zuerst die [CancelUpdate](cancelupdate-method-ado.md)-Methode aufgerufen, um alle zwischengespeicherten Änderungen abzubrechen. Danach werden alle ausstehenden Änderungen im **Recordset** abgebrochen.

Es ist möglich, dass nach einem **CancelBatch** -Aufruf der aktuelle Datensatz nicht ermittelt werden kann, insbesondere, wenn Sie dabei waren, einen neuen Datensatz hinzuzufügen. Aus diesem Grund ist es ratsam, nach dem **CancelBatch** -Aufruf die aktuelle Datensatzposition auf eine bekannte Stelle im **Recordset** festzulegen. Rufen Sie z. B. die [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)-Methode auf.

Wenn der Versuch, die ausstehenden Aktualisierungen abzubrechen, aufgrund eines Konflikts mit den zugrunde liegenden Daten fehlschlägt (z. B. weil ein Datensatz von einem anderen Benutzer gelöscht wurde), werden vom Anbieter Warnungen an die [Errors](errors-collection-ado.md)-Auflistung zurückgegeben, die Programmausführung wird jedoch nicht angehalten. Verwenden Sie die [Filter](filter-property-ado.md)-Eigenschaft (**adFilterAffectedRecord**) und die [Status](status-property-ado-recordset.md)-Eigenschaft, um Datensätze mit Konflikten zu suchen.

