---
title: ADORecordConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b719c6314fb2c68a0a343a800da35ee944654df3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924589"
---
# <a name="adorecordconstruction-interface-ado"></a>ADORecordConstruction-Schnittstelle (ADO)


**Betrifft**: Access 2013, Office 2013

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
<td><p>Lesegeschützt.<br />
Legt den Container eines OLE DB- <strong>Row</strong> -Objekts in ADO <strong>Record</strong> -Objekt fest.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Lese-/Schreibzugriff.<br />
Ruft ein OLE DB- <strong>Row</strong> -Objekt wird aus diesem ADO- <strong>Record</strong> -Objekt zurück oder legt sie fest.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methoden

Keine.

## <a name="events"></a>Ereignisse

Keine.

## <a name="remarks"></a>Hinweise

Ein OLE DB- **Row** -Objekt (pRow), die Konstruktion eines ADO- **Record** -Objekt (), die Konstruktion eines ADO- **Record** -Objekts (AdoR), Mengen an den folgenden drei grundlegenden Schritten zur Verfügung:

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

3.  Rufen Sie die **IADORecordConstruction::put\_Zeile** -Eigenschaftsmethode, um das OLE DB- **Row** -Objekt für das ADO- **Record** -Objekt festzulegen:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
Das resultierende **adoR** -Objekt stellt das **Record** -Objekt von ADO dar, das vom **Row** -Objekt von OLE DB erstellt wurde.

Ein **Record** -Objekt von ADO kann auch im Container eines **Row** -Objekts von OLE DB erstellt werden.

## <a name="requirements"></a>Anforderungen

**Version:** ADO 2.0 und höher

**Bibliothek: msado15.dll**

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

