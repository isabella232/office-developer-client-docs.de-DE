---
title: Zeile - Eigenschaft, ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7578a00719946450e840080c21284784a27be170
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870947"
---
# <a name="row-property-ado"></a>Row-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013



Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest. Bei Verwendung **platzieren\_Zeile** um ein **Row** -Objekt festgelegt, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_Zeile (\[out Retval\] IUnknown\* \* PpRow);

Platzieren Sie HRESULT\_Zeile (\[in\] IUnknown\* pRow);

## <a name="parameters"></a>Parameter

  - *ppRow*

  - Zeiger auf ein OLE DB- **Row** -Objekt.

  - *PRow*

  - Ein OLE DB- **Row** -Objekt.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Betrifft

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

