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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306860"
---
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest. Wenn Sie **\_RowPosition** verwenden, um das **RowPosition** -Objekt festZulegen, verwendet das resultierende **Recordset** -Objekt das **RowPosition** -Objekt, um die aktuelle Zeile zu bestimmen.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get\_RowPosition (\[Out, retval\] IUnknown\* \* ppRowPos);

HRESULT put\_RowPosition (\[in\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRowPos* |Zeiger auf ein OLE DB- **RowPosition** -Objekt.|
|*PRowPos* |Ein OLE DB- **RowPosition** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft festgelegt ist und sich das **Rowset**-Objekt für das **RowPosition**-Objekt vom **Rowset**-Objekt für das **Recordset**-Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter**-Objekt des **RowPosition**-Objekts.

## <a name="applies-to"></a>Gilt für

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

