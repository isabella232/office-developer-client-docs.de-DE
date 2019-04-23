---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287738"
---
# <a name="parentrow-property-ado"></a>ParentRow-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.

Lesegeschützt.

## <a name="syntax"></a>Syntax

HRESULT put\_parentRow (\[in\] IUnknown\* pParent);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*pParent* |Ein Container einer Zeile.|

## <a name="return-values"></a>Rückgabewerte

Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.

## <a name="applies-to"></a>Gilt für

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

