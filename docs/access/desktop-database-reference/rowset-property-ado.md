---
title: Rowset-Eigenschaft (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7be8abbce6828dd202e0c64eec342de9198f7a9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878535"
---
# <a name="rowset-property-ado"></a>Rowset-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013



Ein **Rowset**-OLE DB-Objekt wird aus einem **ADORecordsetConstruction**-Objekt abgerufen oder für dieses festgelegt. Bei Verwendung der Put\_Rowset, das Rowset in ein ADO- **Recordset** -Objekt aktiviert ist.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_Rowset (\[out Retval\] IUnknown\* \* PpRowset);

Platzieren Sie HRESULT\_Rowset (\[in\] IUnknown\* pRowset);

## <a name="parameters"></a>Parameter

  - *ppRowset*

  - Zeiger auf ein OLE DB- **Rowset** -Objekt.

  - *PRowset*

  - Ein OLE DB- **Rowset** -Objekt.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

