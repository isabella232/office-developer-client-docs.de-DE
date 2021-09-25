---
title: DeleteRecord-Methode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8d8107acb9a4335bf0635117bb57626f6a971e24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565513"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Löscht eine durch [Record](record-object-ado.md) dargestellte Entität.

## <a name="syntax"></a>Syntax

*Datensatz*. **DeleteRecord**_Source_, *Async*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. Wenn *Source* ausgelassen wird oder eine leere Zeichenfolge angibt, wird die durch den aktuellen [Datensatz](record-object-ado.md) dargestellte Entität gelöscht. Wenn der Datensatz ein Sammlungsdatensatz ([RecordType](recordtype-property-ado.md) von **adCollectionRecord**, z. B. ein Verzeichnis) ist, werden auch alle untergeordneten Elemente (z. B. Unterverzeichnisse) gelöscht.|
|*Async* |Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass der Löschvorgang asynchron ist.|

## <a name="remarks"></a>HinwBemerkungeneise

Vorgänge in Bezug auf das durch diesen **Record** dargestellte Objekt schlagen möglicherweise fehl, nachdem das Ausführen dieser Methode beendet wurde. Nach dem Aufrufen von **DeleteRecord** sollte **Record** geschlossen werden, da das Verhalten von **Record** in Abhängigkeit davon, wann der Anbieter den **Record** mit der Datenquelle aktualisiert, möglicherweise unvorhersehbar wird.

Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, werden die Ergebnisse dieses Vorgangs nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset,** indem Sie es schließen und erneut öffnen, oder indem Sie die **Methoden Recordset** [Requery](requery-method-ado.md)oder [Update](update-method-ado.md) und [Resync](resync-method-ado.md) ausführen.

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


