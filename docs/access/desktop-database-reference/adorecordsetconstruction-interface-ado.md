---
title: ADORecordsetConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b99fcfe4fadc3dddf5937ba1043875de43e88d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474959"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction-Schnittstelle (ADO)


**Betrifft**: Access 2013 | Office 2013

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
Ruft ein OLE DB- <strong>Kapitel</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>RowPosition</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>Rowset</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methoden

Keine.

## <a name="events"></a>Ereignisse

Keine.

## <a name="remarks"></a>Hinweise

Erhält ein OLE DB- **Rowset** -Objekt (pRowset), den Aufbau einer ADO- **Recordset** -Objekt (), die Konstruktion eines ADO- **Recordset** -Objekt (AdoRs) Beträge den folgenden drei grundlegenden Schritten:

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

3. Rufen Sie die IADORecordsetConstruction::put\_Rowset-Eigenschaftsmethode, um OLE DB-Rowset-Objekt für das ADO-Recordset-Objekt festzulegen:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
Das resultierende Objekt stellt jetzt das ADO- **Recordset** -Objekt von OLE DB- **Rowset** -Objekt erstellt.

Sie können ein **Recordset** -Objekt von ADO auch von einem **Chapter** - oder **RowPosition** -Objekt von OLE DB erstellen.

## <a name="requirements"></a>Anforderungen

- **Version:** ADO 2.0 und höher

- **Bibliothek: msado15.dll**

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

