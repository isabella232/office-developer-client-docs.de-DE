---
title: ParentRow-Eigenschaft (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476126"
---
# <a name="parentrow-property-ado"></a>ParentRow-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013


Legt den Container eines OLE DB- **Row** -Objekts für ein **ADORecordConstruction** -Objekt fest, sodass das übergeordnete Objekt der Zeile in ein ADO- **Record** -Objekt umgewandelt wird.

Lesegeschützt.

## <a name="syntax"></a>Syntax

Platzieren Sie HRESULT\_ParentRow (\[in\] IUnknown\* pParent);

## <a name="parameters"></a>Parameter

  - *pParent*

  - Ein Container einer Zeile.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Betrifft

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

