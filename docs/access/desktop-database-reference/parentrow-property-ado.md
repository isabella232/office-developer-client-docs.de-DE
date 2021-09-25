---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 372ae0fb41887a3b4bf7203070530d9e00215ccb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568670"
---
# <a name="parentrow-property-ado"></a>ParentRow-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.

Lesegeschützt.

## <a name="syntax"></a>Syntax

HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*pParent* |Ein Container einer Zeile.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte zurück, einschließlich S \_ OK und E \_ FAIL.

## <a name="applies-to"></a>Gilt für

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

