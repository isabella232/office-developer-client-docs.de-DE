---
title: DeleteRecord-Methode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293994"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Löscht eine durch [Record](record-object-ado.md) dargestellte Entität.

## <a name="syntax"></a>Syntax

*Record*. **DeleteRecord * * * Quelle*, *Async*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. Wenn *Source* nicht angegeben wird oder eine leere Zeichenfolge angibt, wird die vom aktuellen [Datensatz](record-object-ado.md) dargestellte Entität gelöscht. Wenn es sich bei dem Datensatz um einen[](recordtype-property-ado.md) Auflistungs Daten Satz handelt (RecordType of **adCollectionRecord**, beispielsweise ein Verzeichnis), werden auch alle untergeordneten Elemente (beispielsweise Unterverzeichnisse) gelöscht.|
|*Async* |Optional. Ein **Boolean** -Wert, der im Fall von **True** angibt, dass der Löschvorgang asynchron ist.|

## <a name="remarks"></a>Bemerkungen

Vorgänge in Bezug auf das durch diesen **Record** dargestellte Objekt schlagen möglicherweise fehl, nachdem das Ausführen dieser Methode beendet wurde. Nach dem Aufrufen von **DeleteRecord** sollte **Record** geschlossen werden, da das Verhalten von **Record** in Abhängigkeit davon, wann der Anbieter den **Record** mit der Datenquelle aktualisiert, möglicherweise unvorhersehbar wird.

Wurde dieser **Record** aus einem [Recordset](recordset-object-ado.md)-Objekt abgerufen, werden die Ergebnisse dieses Vorgangs nicht unmittelbar im **Recordset** -Objekt wiedergegeben. Aktualisieren Sie das **Recordset** -Objekt, indem Sie es schließen und erneut öffnen, oder indem Sie die **Recordset** [Requery](requery-method-ado.md)-oder [Update](update-method-ado.md) -und Resync-Methoden ausführen. [](resync-method-ado.md)

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).


