---
<<<<<<< HEAD-Titel: RowPosition-Eigenschaft (ADO) TOCTitle: RowPosition-Eigenschaft (ADO) === Titel: RowPosition-Eigenschaft (ADO) TOCTitle: RowPosition-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) Ms:contentKeyID: 48547325 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)
=======
# <a name="rowposition-property-ado"></a>RowPosition-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013



Ruft ein OLE DB- **RowPosition** -Objekt aus einem **ADORecordsetConstruction** -Objekt ab oder legt es dafür fest. Bei Verwendung **platzieren\_RowPosition** zur **RowPosition** -Objekt das resultierende **Recordset** -Objekt verwendet das **RowPosition** -Objekt zum Bestimmen der aktuellen Zeile.

Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

HRESULT Get\_RowPosition (\[out Retval\] IUnknown\* \* PpRowPos);

Platzieren Sie HRESULT\_RowPosition (\[in\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parameter

  - *ppRowPos*

  - Zeiger auf ein OLE DB- **RowPosition** -Objekt.

  - *PRowPos*

  - Ein OLE DB- **RowPosition** -Objekt.

<<<<<<< Kopf
## <a name="return-values"></a>Rückgabewert
=======
## <a name="return-values"></a>Rückgabewerte
>>>>>>> master

Diese Eigenschaftsmethode gibt die HRESULT-Standardwerte, einschließlich S\_OK und E\_fehl.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft festgelegt ist und sich das **Rowset** -Objekt für das **RowPosition** -Objekt vom **Rowset** -Objekt für das **Recordset** -Objekt unterscheidet, wird letzteres überschrieben. Dasselbe Verhalten gilt auch für das aktuelle **Chapter** -Objekt des **RowPosition** -Objekts.

## <a name="applies-to"></a>Betrifft

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

