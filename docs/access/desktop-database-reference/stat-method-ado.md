---
title: Stat-Methode – ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308549"
---
# <a name="stat-method-ado"></a><span data-ttu-id="18c16-102">Stat-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="18c16-102">Stat method (ADO)</span></span>

<span data-ttu-id="18c16-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18c16-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18c16-104">Ruft Informationen zu einem **Stream**-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="18c16-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18c16-105">Syntax</span></span>

<span data-ttu-id="18c16-106">Long- *Stream*. Stat (*StatStg*, *StatFlag*)</span><span class="sxs-lookup"><span data-stu-id="18c16-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="18c16-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18c16-107">Return value</span></span>

<span data-ttu-id="18c16-108">Ein langer Wert, der den Status des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="18c16-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="18c16-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="18c16-109">Parameters</span></span>

|<span data-ttu-id="18c16-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="18c16-110">Parameter</span></span>|<span data-ttu-id="18c16-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18c16-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="18c16-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="18c16-112">*StatStg*</span></span> |<span data-ttu-id="18c16-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span><span class="sxs-lookup"><span data-stu-id="18c16-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="18c16-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="18c16-115">*StatFlag*</span></span> |<span data-ttu-id="18c16-p102">Gibt an, dass diese Methode einige Member in der STATSTG-Struktur nicht zurückgibt und daher einen Speicherzuweisungsvorgang speichert. Die Werte werden der STATFLAG-Enumeration entnommen.</span><span class="sxs-lookup"><span data-stu-id="18c16-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="18c16-118">Die STATFLAG-Aufzählung hat zwei Werte:</span><span class="sxs-lookup"><span data-stu-id="18c16-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="18c16-119">-STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="18c16-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="18c16-120">-STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="18c16-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="18c16-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18c16-121">Remarks</span></span>

<span data-ttu-id="18c16-122">Die Version der Stat-Methode, die für das Stream-Objekt in ADO implementiert wurde, füllt die folgenden Felder der STATSTG-Struktur aus:</span><span class="sxs-lookup"><span data-stu-id="18c16-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="18c16-123">Feld</span><span class="sxs-lookup"><span data-stu-id="18c16-123">Field</span></span>|<span data-ttu-id="18c16-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18c16-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="18c16-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="18c16-125">*pwcsName*</span></span> |<span data-ttu-id="18c16-126">Eine Zeichenfolge mit dem Namen des Streams, sofern vorhanden, und der StatFlag-Wert STATFLAG\_Noname wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="18c16-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="18c16-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="18c16-127">*cbSize*</span></span> |<span data-ttu-id="18c16-128">Gibt die Größe des Datenstroms oder des Bytearrays in Byte an.</span><span class="sxs-lookup"><span data-stu-id="18c16-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="18c16-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="18c16-129">*mtime*</span></span> |<span data-ttu-id="18c16-130">Gibt den Zeitpunkt der letzten Änderung dieses Speichers, Datenstroms oder Bytearrays an.</span><span class="sxs-lookup"><span data-stu-id="18c16-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="18c16-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="18c16-131">*ctime*</span></span> |<span data-ttu-id="18c16-132">Gibt den Zeitpunkt der Erstellung dieses Speichers, Datenstroms oder Bytearrays an.</span><span class="sxs-lookup"><span data-stu-id="18c16-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="18c16-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="18c16-133">*atime*</span></span> |<span data-ttu-id="18c16-134">Gibt den Zeitpunkt des letzten Zugriffs auf diesen Speicher, diesen Datenstrom oder dieses Bytearray an.</span><span class="sxs-lookup"><span data-stu-id="18c16-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="18c16-135">Wenn STATFLAG\_Noname im STATFLAG-Parameter angegeben ist, wird der Name des Streams nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="18c16-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="18c16-136">Wenn STATFLAG\_Noname nicht im STATFLAG-Parameter angegeben wurde und kein Name für den aktuellen Stream verfügbar ist, ist dieser Wert E\_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="18c16-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

