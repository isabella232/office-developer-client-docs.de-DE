---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306741"
---
# <a name="rowset-property-ado"></a>Rowset-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object. Wenn Sie put\_-Rowset verwenden, wird das Rowset in ein ADO- **Recordset** -Objekt umgewandelt.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get\_-Rowset\[(Out,\] retval\* \* IUnknown ppRowset);

HRESULT put\_-Rowset\[(\] in\* IUnknown pRowset);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRowset* |Zeiger auf ein OLE DB- **Rowset** -Objekt.|
|*PRowset* |Ein OLE DB- **Rowset** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.

## <a name="applies-to"></a>Gilt für

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

