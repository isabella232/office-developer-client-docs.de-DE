---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296395"
---
# <a name="chapter-property-ado"></a>Chapter-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013
 
Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object. Wenn Sie das **Chapter** -Objekt mithilfe von " **\_Chapter** " festlegen, wird eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt umgewandelt. This sets the current chapter of the **Rowset** object. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT get\_Chapter (\[Out, retval\] Long\* plChapter);

HRESULT put\_Chapter (\[in\] Long lChapter);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*plChapter* |Zeiger auf das Handle eines Kapitels.|
|*LChapter* |Handle eines Kapitels.|

## <a name="return-values"></a>Rückgabewerte

Diese Property-Methode gibt die standardmäßigen HRESULT-\_Werte zurück,\_einschließlich S OK und e Fail.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

