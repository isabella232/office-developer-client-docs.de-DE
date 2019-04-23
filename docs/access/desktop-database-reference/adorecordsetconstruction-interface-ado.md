---
title: ADORecordsetConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281633"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction-Schnittstelle (ADO)


**Gilt für**: Access 2013, Office 2013

Mit der **ADORecordsetConstruction** -Schnittstelle wird ein **Recordset** -Objekt von ADO von einem **Rowset** -Objekt von OLE DB in einer C/C++-Anwendung erstellt.

Diese Schnittstelle unterstützt die folgenden Eigenschaften:

## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Kapitel</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>Chapter</strong> -Objekt aus/für dieses ADO- <strong>Recordset</strong> -Objekt ab.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>RowPosition</strong> -Objekt aus/für dieses ADO- <strong>Recordset</strong> -Objekt ab.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>Rowsetobjekt</strong> aus diesem ADO- <strong>Recordset</strong> -Objekt ab, oder legt dieses fest.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methoden

Keine.

## <a name="events"></a>Ereignisse

Keine.

## <a name="remarks"></a>Bemerkungen

Bei einem OLE DB **** -Rowsetobjekt (pRowset) wird die Erstellung eines ADO- **Recordset** -Objekts () durch die Erstellung eines ADO- **Recordset** -Objekts (adoRS) auf die folgenden drei grundlegenden Vorgänge festgestellt:

1. Erstellen eines **Recordset** -Objekts von ADO:
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Abfragen der **IADORecordsetConstruction** -Schnittstelle im **Recordset** -Objekt:

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Rufen Sie die IADORecordsetConstruction::p\_UT-Rowset-Eigenschaftsmethode auf, um das OLE DB-Rowsetobjekt für das ADO-Recordset-Objekt festzulegen:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
Das resultierende Objekt stellt jetzt das ADO- **Recordset** -Objekt dar, das aus dem OLE DB- **Rowsetobjekt** erstellt wurde.

Sie können ein **Recordset**-Objekt von ADO auch von einem **Chapter**- oder **RowPosition**-Objekt von OLE DB erstellen.

## <a name="requirements"></a>Anforderungen

- **Version:** ADO 2.0 und höher

- **Bibliothek: msado15.dll**

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

