---
title: Row-Eigenschaft – ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c21d714c13fb3b706f932e3cb1248f2d4e2874f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611581"
---
# <a name="row-property-ado"></a>Row-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest. Wenn Sie **Row \_** zum Festlegen eines **Row-Objekts** verwenden, wird eine Zeile in ein ADO **Record-Objekt** umgewandelt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);

HRESULT put \_ Row( \[ in \] IUnknown \* pRow);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRow* |Zeiger auf ein OLE DB- **Row** -Objekt.|
|*PRow* |Ein OLE DB- **Row** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte zurück, einschließlich S \_ OK und E \_ FAIL.

## <a name="applies-to"></a>Gilt für

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

