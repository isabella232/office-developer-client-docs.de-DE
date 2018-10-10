---
title: Chapter-Eigenschaft (ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475221"
---
# <a name="chapter-property-ado"></a>Chapter-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013
 

Ein **Chapter**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt. Bei Verwendung **platzieren\_Kapitel** , um das **Kapitel** -Objekt festzulegen, eine Teilmenge von Zeilen in ein ADO- **Recordset** -Objekt aktiviert ist. Hierdurch wird das aktuelle Kapitel des **Rowset** -Objekt. Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_Kapitel (\[out Retval\] lang\* PlChapter);

Platzieren Sie HRESULT\_Kapitel (\[in\] lang lChapter);

## <a name="parameters"></a>Parameter

  - *plChapter*

  - Zeiger auf das Handle eines Kapitels.

  - *LChapter*

  - Handle eines Kapitels.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

