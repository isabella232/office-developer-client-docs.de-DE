---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1732e32e784f84ab6b21855f94c5b326420cfe41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618511"
---
# <a name="chapter-property-ado"></a>Chapter-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013
 
Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object. Wenn Sie **\_ "Put Chapter"** zum Festlegen des **Chapter-Objekts** verwenden, wird eine Teilmenge von Zeilen in ein **ADO-Recordset-Objekt** umgewandelt. This sets the current chapter of the **Rowset** object. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);

HRESULT put \_ Chapter( \[ in long \] lChapter);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*plChapter* |Zeiger auf das Handle eines Kapitels.|
|*LChapter* |Handle eines Kapitels.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte zurück, einschließlich S \_ OK und E \_ FAIL.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

