---
title: ADORecordConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ddf7da4e99f852178e0d12484e86f54248b4185
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874559"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="916d8-102">ADORecordConstruction-Schnittstelle (ADO)</span><span class="sxs-lookup"><span data-stu-id="916d8-102">ADORecordConstruction Interface (ADO)</span></span>


<span data-ttu-id="916d8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="916d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="916d8-104">Mit der **ADORecordConstruction** -Schnittstelle wird ein **Record** -Objekt von ADO von einem **Row** -Objekt von OLE DB in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="916d8-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="916d8-105">Diese Schnittstelle unterstützt die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="916d8-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="916d8-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="916d8-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="916d8-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="916d8-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="916d8-108">Lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="916d8-108">Write-only.</span></span><br />
<span data-ttu-id="916d8-109">Legt den Container eines OLE DB- <strong>Row</strong> -Objekts in ADO <strong>Record</strong> -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="916d8-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="916d8-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="916d8-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="916d8-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="916d8-111">Read/Write.</span></span><br />
<span data-ttu-id="916d8-112">Ruft ein OLE DB- <strong>Row</strong> -Objekt wird aus diesem ADO- <strong>Record</strong> -Objekt zurück oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="916d8-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="916d8-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="916d8-113">Methods</span></span>

<span data-ttu-id="916d8-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="916d8-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="916d8-115">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="916d8-115">Events</span></span>

<span data-ttu-id="916d8-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="916d8-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="916d8-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="916d8-117">Remarks</span></span>

<span data-ttu-id="916d8-118">Ein OLE DB- **Row** -Objekt (pRow), die Konstruktion eines ADO- **Record** -Objekt (), die Konstruktion eines ADO- **Record** -Objekts (AdoR), Mengen an den folgenden drei grundlegenden Schritten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="916d8-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="916d8-119">Erstellen eines **Record** -Objekts von ADO:</span><span class="sxs-lookup"><span data-stu-id="916d8-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="916d8-120">Abfragen der **IADORecordConstruction** -Schnittstelle im **Record** -Objekt:</span><span class="sxs-lookup"><span data-stu-id="916d8-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="916d8-121">Rufen Sie die **IADORecordConstruction::put\_Zeile** -Eigenschaftsmethode, um das OLE DB- **Row** -Objekt für das ADO- **Record** -Objekt festzulegen:</span><span class="sxs-lookup"><span data-stu-id="916d8-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="916d8-122">Das resultierende **adoR** -Objekt stellt das **Record** -Objekt von ADO dar, das vom **Row** -Objekt von OLE DB erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="916d8-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="916d8-123">Ein **Record** -Objekt von ADO kann auch im Container eines **Row** -Objekts von OLE DB erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="916d8-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="916d8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="916d8-124">Requirements</span></span>

<span data-ttu-id="916d8-125">**Version:** ADO 2.0 und höher</span><span class="sxs-lookup"><span data-stu-id="916d8-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="916d8-126">**Bibliothek: msado15.dll**</span><span class="sxs-lookup"><span data-stu-id="916d8-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="916d8-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="916d8-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

