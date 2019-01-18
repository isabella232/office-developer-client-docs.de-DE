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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717937"
---
# <a name="chapter-property-ado"></a>Chapter-Eigenschaft (ADO)

**Betrifft**: Access 2013, Office 2013
 
Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt. Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist. Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);

Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*plChapter* |Zeiger auf das Handle eines Kapitels.|
|*LChapter* |Handle eines Kapitels.|

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

