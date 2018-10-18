---
title: STAT-Methode - ActiveX Data Objects (ADO)
TOCTitle: Stat Method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc4ff8076ec07d065ba932ef0e0017edb97e703
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606955"
---
# <a name="stat-method-ado"></a><span data-ttu-id="50c26-102">Stat-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="50c26-102">Stat Method (ADO)</span></span>


<span data-ttu-id="50c26-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="50c26-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="50c26-104">Ruft Informationen zu einem **Stream** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="50c26-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c26-105">Syntax</span></span>

<span data-ttu-id="50c26-106">Lange *Stream*. STAT (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="50c26-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

<span data-ttu-id="50c26-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="50c26-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="50c26-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50c26-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="50c26-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50c26-109">Return value</span></span>
>>>>>>> <span data-ttu-id="50c26-110">master</span><span class="sxs-lookup"><span data-stu-id="50c26-110">master</span></span>

<span data-ttu-id="50c26-111">Ein langer Wert, der den Status des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="50c26-111">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="50c26-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="50c26-112">Parameters</span></span>

  - <span data-ttu-id="50c26-113">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="50c26-113">*StatStg*</span></span>

  - <span data-ttu-id="50c26-p101">Eine STATSTG-Struktur, die mit Informationen zum Datenstrom ausgefüllt wird. Die Implementierung der Stat-Methode, die vom Stream-Objekt in ADO verwendet wird, füllt nicht alle Felder der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="50c26-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>

  - <span data-ttu-id="50c26-116">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="50c26-116">*StatFlag*</span></span>

  - <span data-ttu-id="50c26-p102">Gibt an, dass diese Methode einige Member in der STATSTG-Struktur nicht zurückgibt und daher einen Speicherzuweisungsvorgang speichert. Die Werte werden der STATFLAG-Enumeration entnommen.</span><span class="sxs-lookup"><span data-stu-id="50c26-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span>  
      
    <span data-ttu-id="50c26-119">Die STATFLAG-Enumeration weist zwei Werte auf:</span><span class="sxs-lookup"><span data-stu-id="50c26-119">The STATFLAG enumeration has two values</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="50c26-120">Konstante</span><span class="sxs-lookup"><span data-stu-id="50c26-120">Constant</span></span></p></th>
    <th><p><span data-ttu-id="50c26-121">Wert</span><span class="sxs-lookup"><span data-stu-id="50c26-121">Value</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="50c26-122">STATFLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="50c26-122">STATFLAG_DEFAULT</span></span></p></td>
    <td><p><span data-ttu-id="50c26-123">0</span><span class="sxs-lookup"><span data-stu-id="50c26-123">0</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="50c26-124">STATFLAG_NONAME</span><span class="sxs-lookup"><span data-stu-id="50c26-124">STATFLAG_NONAME</span></span></p></td>
    <td><p><span data-ttu-id="50c26-125">1</span><span class="sxs-lookup"><span data-stu-id="50c26-125">1</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="50c26-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50c26-126">Remarks</span></span>

<span data-ttu-id="50c26-127">Die Version der Stat-Methode, die für das Stream-Objekt in ADO implementiert wurde, füllt die folgenden Felder der STATSTG-Struktur aus:</span><span class="sxs-lookup"><span data-stu-id="50c26-127">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

  - <span data-ttu-id="50c26-128">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="50c26-128">*pwcsName*</span></span>

  - <span data-ttu-id="50c26-129">Eine Zeichenfolge mit dem Namen des Stream-Objekts, wenn eine verfügbar ist und der StatFlag-Wert STATFLAG\_NONAME nicht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="50c26-129">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>

  - <span data-ttu-id="50c26-130">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="50c26-130">*cbSize*</span></span>

  - <span data-ttu-id="50c26-131">Gibt die Größe des Datenstroms oder des Bytearrays in Byte an.</span><span class="sxs-lookup"><span data-stu-id="50c26-131">Specifies the size in bytes of the stream or byte array.</span></span>

  - <span data-ttu-id="50c26-132">*mtime*</span><span class="sxs-lookup"><span data-stu-id="50c26-132">*mtime*</span></span>

  - <span data-ttu-id="50c26-133">Gibt den Zeitpunkt der letzten Änderung dieses Speichers, Datenstroms oder Bytearrays an.</span><span class="sxs-lookup"><span data-stu-id="50c26-133">Indicates the last modification time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="50c26-134">*ctime*</span><span class="sxs-lookup"><span data-stu-id="50c26-134">*ctime*</span></span>

  - <span data-ttu-id="50c26-135">Gibt den Zeitpunkt der Erstellung dieses Speichers, Datenstroms oder Bytearrays an.</span><span class="sxs-lookup"><span data-stu-id="50c26-135">Indicates the creation time for this storage, stream, or byte array.</span></span>

  - <span data-ttu-id="50c26-136">*atime*</span><span class="sxs-lookup"><span data-stu-id="50c26-136">*atime*</span></span>

  - <span data-ttu-id="50c26-137">Gibt den Zeitpunkt des letzten Zugriffs auf diesen Speicher, diesen Datenstrom oder dieses Bytearray an.</span><span class="sxs-lookup"><span data-stu-id="50c26-137">Indicates the last access time for this storage, stream or byte array.</span></span>

<span data-ttu-id="50c26-138">Wenn STATFLAG\_NONAME im StatFlag-Parameter angegeben ist, wird der Name des Datenstroms nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50c26-138">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="50c26-139">Wenn STATFLAG\_NONAME im StatFlag-Parameter nicht angegeben wurde und kein Name vorhanden ist, für den aktuellen Datenstrom, lautet dieser Wert E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="50c26-139">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

