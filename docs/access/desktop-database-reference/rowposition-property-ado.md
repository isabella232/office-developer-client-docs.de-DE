---
title: RowPosition-Eigenschaft (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 26ef8dc573e548dbdb2d35d53bd470df63ce17f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615039"
---
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest. Wenn Sie **\_ Put RowPosition** zum Festlegen des **RowPosition-Objekts** verwenden, verwendet das resultierende **Recordset-Objekt** das **RowPosition-Objekt,** um die aktuelle Zeile zu bestimmen.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRowPos* |Zeiger auf ein OLE DB- **RowPosition** -Objekt.|
|*PRowPos* |Ein OLE DB- **RowPosition** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte zurück, einschließlich S \_ OK und E \_ FAIL.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft festgelegt ist und sich das **Rowset**-Objekt für das **RowPosition**-Objekt vom **Rowset**-Objekt für das **Recordset**-Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter**-Objekt des **RowPosition**-Objekts.

## <a name="applies-to"></a>Gilt für

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

