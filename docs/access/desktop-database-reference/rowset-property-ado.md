---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ad31c4b34f4e94329907264e8ed29eddc08dbecb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615011"
---
# <a name="rowset-property-ado"></a>Rowset-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object. Wenn Sie \_ "put"-Rowset verwenden, wird das Rowset in ein **ADO-Recordset-Objekt** umgewandelt.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get \_ Rowset( \[ out, retval \] IUnknown \* \* ppRowset);

HRESULT put \_ Rowset( \[ in \] IUnknown \* pRowset);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRowset* |Zeiger auf ein OLE DB- **Rowset** -Objekt.|
|*PRowset* |Ein OLE DB- **Rowset** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte zurück, einschließlich S \_ OK und E \_ FAIL.

## <a name="applies-to"></a>Gilt für

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

