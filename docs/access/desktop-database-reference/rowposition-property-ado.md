---
title: RowPosition-Eigenschaft (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720961"
---
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest. Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);

Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRowPos* |Zeiger auf ein OLE DB- **RowPosition** -Objekt.|
|*PRowPos* |Ein OLE DB- **RowPosition** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.

## <a name="applies-to"></a>Gilt für

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

