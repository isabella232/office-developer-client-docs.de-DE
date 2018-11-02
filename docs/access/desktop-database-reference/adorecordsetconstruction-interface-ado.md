---
title: ADORecordsetConstruction-Schnittstelle (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ab9723d3acc698aa36210e26e370c0edfa67728
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924232"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="6be15-102">ADORecordsetConstruction-Schnittstelle (ADO)</span><span class="sxs-lookup"><span data-stu-id="6be15-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="6be15-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6be15-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6be15-104">Mit der **ADORecordsetConstruction** -Schnittstelle wird ein **Recordset** -Objekt von ADO von einem **Rowset** -Objekt von OLE DB in einer C/C++-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="6be15-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="6be15-105">Diese Schnittstelle unterstützt die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6be15-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="6be15-106">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6be15-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be15-107"><a href="chapter-property-ado.md">Kapitel</a></span><span class="sxs-lookup"><span data-stu-id="6be15-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="6be15-108">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6be15-108">Read/Write.</span></span><br />
<span data-ttu-id="6be15-109">Ruft ein OLE DB- <strong>Kapitel</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6be15-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be15-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="6be15-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="6be15-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6be15-111">Read/Write.</span></span><br />
<span data-ttu-id="6be15-112">Ruft ein OLE DB- <strong>RowPosition</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6be15-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be15-113"><a href="rowset-property-ado.md">Rowset</a></span><span class="sxs-lookup"><span data-stu-id="6be15-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="6be15-114">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6be15-114">Read/Write.</span></span><br />
<span data-ttu-id="6be15-115">Ruft ein OLE DB- <strong>Rowset</strong> -Objekt wird von diesem ADO- <strong>Recordset</strong> -Objekt zurück oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="6be15-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="6be15-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="6be15-116">Methods</span></span>

<span data-ttu-id="6be15-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="6be15-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="6be15-118">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6be15-118">Events</span></span>

<span data-ttu-id="6be15-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="6be15-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be15-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6be15-120">Remarks</span></span>

<span data-ttu-id="6be15-121">Erhält ein OLE DB- **Rowset** -Objekt (pRowset), den Aufbau einer ADO- **Recordset** -Objekt (), die Konstruktion eines ADO- **Recordset** -Objekt (AdoRs) Beträge den folgenden drei grundlegenden Schritten:</span><span class="sxs-lookup"><span data-stu-id="6be15-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="6be15-122">Erstellen eines **Recordset** -Objekts von ADO:</span><span class="sxs-lookup"><span data-stu-id="6be15-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="6be15-123">Abfragen der **IADORecordsetConstruction** -Schnittstelle im **Recordset** -Objekt:</span><span class="sxs-lookup"><span data-stu-id="6be15-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="6be15-124">Rufen Sie die IADORecordsetConstruction::put\_Rowset-Eigenschaftsmethode, um OLE DB-Rowset-Objekt für das ADO-Recordset-Objekt festzulegen:</span><span class="sxs-lookup"><span data-stu-id="6be15-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="6be15-125">Das resultierende Objekt stellt jetzt das ADO- **Recordset** -Objekt von OLE DB- **Rowset** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="6be15-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="6be15-126">Sie können ein **Recordset** -Objekt von ADO auch von einem **Chapter** - oder **RowPosition** -Objekt von OLE DB erstellen.</span><span class="sxs-lookup"><span data-stu-id="6be15-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be15-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6be15-127">Requirements</span></span>

- <span data-ttu-id="6be15-128">**Version:** ADO 2.0 und höher</span><span class="sxs-lookup"><span data-stu-id="6be15-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="6be15-129">**Bibliothek: msado15.dll**</span><span class="sxs-lookup"><span data-stu-id="6be15-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="6be15-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="6be15-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

