---
title: Row-Eigenschaft-ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306482"
---
# <a name="row-property-ado"></a>Row-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Ruft ein **Row** -Objekt von OLE DB aus einem **ADORecordConstruction** -Objekt ab oder legt es dafür fest. Wenn Sie zum Festlegen eines **Row** -Objekts die **\_Put-Zeile** verwenden, wird eine Zeile in ein ADO- **Record** -Objekt umgewandelt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get\_Row (\[Out, retval\] IUnknown\* \* ppRow);

\_Zeile mit HRESULT (\[in\] IUnknown\* Bug);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ppRow* |Zeiger auf ein OLE DB- **Row** -Objekt.|
|*PRow* |Ein OLE DB- **Row** -Objekt.|

## <a name="return-values"></a>Rückgabewerte

Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.

## <a name="applies-to"></a>Gilt für

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

