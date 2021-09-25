---
title: ADORecordsetConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fb31007a8dc1a1471219a5849924e147aab41778
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559213"
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
Ruft ein OLE <strong>DB-Kapitelobjekt</strong> aus/für dieses <strong>ADO-Recordset-Objekt</strong> ab/legt es fest.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB <strong>RowPosition</strong> -Objekt aus/für dieses <strong>ADO-Recordset-Objekt</strong> ab/legt dieses fest.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE <strong>DB-Rowset-Objekt</strong> aus/für dieses <strong>ADO-Recordset-Objekt</strong> ab/legt es fest.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methoden

Keine.

## <a name="events"></a>Ereignisse

Keine.

## <a name="remarks"></a>HinwBemerkungeneise

Bei einem OLE **DB-Rowset-Objekt** (pRowset), der Erstellung eines **ADO-Recordset-Objekts** (), entspricht die Erstellung eines **ADO-Recordset-Objekts** (adoRs) den folgenden drei grundlegenden Vorgängen:

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

3. Rufen Sie die IADORecordsetConstruction::p ut \_ Rowset-Eigenschaftsmethode auf, um das OLE DB-Rowset-Objekt für das ADO-Recordset-Objekt festzulegen:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
Das resultierende Objekt stellt nun das aus dem OLE **DB-Rowset-Objekt** erstellte **ADO-Recordset-Objekt** dar.

Sie können ein **Recordset**-Objekt von ADO auch von einem **Chapter**- oder **RowPosition**-Objekt von OLE DB erstellen.

## <a name="requirements"></a>Anforderungen

- **Version:** ADO 2.0 und höher

- **Bibliothek: msado15.dll**

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

