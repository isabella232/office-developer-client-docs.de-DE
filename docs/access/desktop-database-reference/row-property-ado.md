---
title: Zeile - Eigenschaft, ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715004"
---
# <a name="row-property-ado"></a>Row-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013

Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest. Bei Verwendung **platzieren\_Zeile** um ein **Row** -Objekt festgelegt, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_Zeile (\[out Retval\] IUnknown\* \* PpRow);

Platzieren Sie HRESULT\_Zeile (\[in\] IUnknown\* pRow);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRow* |Zeiger auf ein OLE DB- **Row** -Objekt.|
|*PRow* |Ein OLE DB- **Row** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Gilt für

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

