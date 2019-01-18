---
title: ADORecordConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712008"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="0255e-102">ADORecordConstruction-Schnittstelle (ADO)</span><span class="sxs-lookup"><span data-stu-id="0255e-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="0255e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0255e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0255e-104">Mit der **ADORecordConstruction** -Schnittstelle wird ein **Record** -Objekt von ADO von einem **Row** -Objekt von OLE DB in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0255e-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="0255e-105">Diese Schnittstelle unterstützt die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0255e-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="0255e-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0255e-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0255e-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="0255e-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="0255e-108">Lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="0255e-108">Write-only.</span></span><br />
<span data-ttu-id="0255e-109">Legt den Container eines OLE DB- <strong>Row</strong> -Objekts in ADO <strong>Record</strong> -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="0255e-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0255e-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="0255e-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="0255e-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0255e-111">Read/Write.</span></span><br />
<span data-ttu-id="0255e-112">Ruft ein OLE DB- <strong>Row</strong> -Objekt wird aus diesem ADO- <strong>Record</strong> -Objekt zurück oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="0255e-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="0255e-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0255e-113">Methods</span></span>

<span data-ttu-id="0255e-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="0255e-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="0255e-115">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="0255e-115">Events</span></span>

<span data-ttu-id="0255e-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="0255e-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0255e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0255e-117">Remarks</span></span>

<span data-ttu-id="0255e-118">Ein OLE DB- **Row** -Objekt (pRow), die Konstruktion eines ADO- **Record** -Objekt (), die Konstruktion eines ADO- **Record** -Objekts (AdoR), Mengen an den folgenden drei grundlegenden Schritten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="0255e-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="0255e-119">Erstellen eines **Record** -Objekts von ADO:</span><span class="sxs-lookup"><span data-stu-id="0255e-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="0255e-120">Abfragen der **IADORecordConstruction** -Schnittstelle im **Record** -Objekt:</span><span class="sxs-lookup"><span data-stu-id="0255e-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="0255e-121">Rufen Sie die **IADORecordConstruction::put\_Zeile** -Eigenschaftsmethode, um das OLE DB- **Row** -Objekt für das ADO- **Record** -Objekt festzulegen:</span><span class="sxs-lookup"><span data-stu-id="0255e-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="0255e-122">Das resultierende **adoR** -Objekt stellt das **Record** -Objekt von ADO dar, das vom **Row** -Objekt von OLE DB erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0255e-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="0255e-123">Ein **Record** -Objekt von ADO kann auch im Container eines **Row** -Objekts von OLE DB erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0255e-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0255e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0255e-124">Requirements</span></span>

<span data-ttu-id="0255e-125">**Version:** ADO 2.0 und höher</span><span class="sxs-lookup"><span data-stu-id="0255e-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="0255e-126">**Bibliothek: msado15.dll**</span><span class="sxs-lookup"><span data-stu-id="0255e-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="0255e-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="0255e-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

