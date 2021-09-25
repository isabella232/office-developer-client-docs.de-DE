---
title: ADORecordConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2b223e10e6ed8450a881225b76b01761436b12ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607535"
---
# <a name="adorecordconstruction-interface-ado"></a>ADORecordConstruction-Schnittstelle (ADO)


**Gilt für**: Access 2013, Office 2013

Mit der **ADORecordConstruction** -Schnittstelle wird ein **Record** -Objekt von ADO von einem **Row** -Objekt von OLE DB in einer C/C++-Anwendung erstellt.

Diese Schnittstelle unterstützt die folgenden Eigenschaften:

## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Schreibzugriff.<br />

Legt den Container eines <strong>Row</strong>-Objekts von OLE DB auf dieses <strong>Record</strong>-Objekt von ADO fest.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB <strong>Row</strong> -Objekt aus/für dieses ADO <strong>Record</strong> -Objekt ab/legt dieses fest.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methoden

Keine.

## <a name="events"></a>Ereignisse

Keine.

## <a name="remarks"></a>HinwBemerkungeneise

Bei einem OLE DB **Row-Objekt** (pRow) entspricht die Erstellung eines ADO **Record-Objekts** (), der Konstruktion eines ADO **Record-Objekts** (adoR), den folgenden drei grundlegenden Vorgängen:

1.  Erstellen eines **Record** -Objekts von ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Abfragen der **IADORecordConstruction** -Schnittstelle im **Record** -Objekt:
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Rufen Sie die **IADORecordConstruction::p ut \_ Row-Eigenschaftsmethode** auf, um das OLE DB **Row-Objekt** für das ADO **Record-Objekt** festzulegen:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
Das resultierende **adoR** -Objekt stellt das **Record** -Objekt von ADO dar, das vom **Row** -Objekt von OLE DB erstellt wurde.

Ein **Record**-Objekt von ADO kann auch im Container eines **Row**-Objekts von OLE DB erstellt werden.

## <a name="requirements"></a>Anforderungen

**Version:** ADO 2.0 und höher

**Bibliothek: msado15.dll**

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

