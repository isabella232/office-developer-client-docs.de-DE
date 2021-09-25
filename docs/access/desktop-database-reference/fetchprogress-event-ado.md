---
title: FetchProgress-Ereignis (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 32aca282a3ef79ad5e29614445559a653034528a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602672"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress-Ereignis (ADO)

**Gilt für**: Access 2013, Office 2013

Das **FetchProgress**-Ereignis wird regelmäßig während einer langen asynchronen Operation aufgerufen, um einen Bericht darüber zu erstellen, wie viele zusätzliche Zeilen derzeit in das [Recordset](recordset-object-ado.md) abgerufen wurden.

## <a name="syntax"></a>Syntax

FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Progress* |Ein **Long** -Wert, der die Anzahl von Datensätzen angibt, die derzeit mit der Fetch-Operation abgerufen wurden.|
|*MaxProgress* |Ein **Long** -Wert, der die maximale Anzahl von Datensätzen angibt, die erwartungsgemäß abgerufen werden.|
|*adStatus* |Ein [EventStatusEnum](eventstatusenum.md)-Statuswert.|
|*pRecordset* |Ein **Recordset** -Objekt, das das Objekt darstellt, für das die Datensätze abgerufen werden.|

## <a name="remarks"></a>HinwBemerkungeneise

Wenn **FetchProgress** mit einem untergeordneten **Recordset**-Objekt verwendet wird, ist zu beachten, dass die *Progress*- und *MaxProgress*-Parameterwerte vom zugrunde liegenden [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)-Rowset abgeleitet werden. Die zurückgegebenen Werte stellen die Gesamtanzahl von Datensätzen im zugrunde liegenden Rowset dar, nicht nur die Anzahl von Datensätzen im aktuellen Kapitel.

> [!NOTE]
> [!HINWEIS] Um **FetchProgress** mit Microsoft Visual Basic zu verwenden, ist Visual Basic 6.0 oder höher erforderlich.


