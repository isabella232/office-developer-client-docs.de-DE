---
title: Read-Methode - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473815"
---
# <a name="read-method-ado"></a><span data-ttu-id="24782-102">Read-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="24782-102">Read Method (ADO)</span></span>


<span data-ttu-id="24782-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24782-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="24782-104">Liest eine angegebene Anzahl von Bytes aus einem binären [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="24782-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="24782-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24782-105">Syntax</span></span>

<span data-ttu-id="24782-106">*Variant* = *Stream-Objekt*. Lesen (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="24782-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="24782-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="24782-107">Parameters</span></span>

  - <span data-ttu-id="24782-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="24782-108">*NumBytes*</span></span>

  - <span data-ttu-id="24782-p101">Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Bytes oder den [StreamReadEnum](streamreadenum.md)-Wert **adReadAll** angibt. Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="24782-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="24782-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24782-111">Return Value</span></span>

<span data-ttu-id="24782-112">Die **Read** -Methode liest eine angegebene Anzahl von Bytes oder den gesamten Datenstrom aus einem **Stream** -Objekt und gibt die resultierenden Daten als einen **Variant** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24782-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24782-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24782-113">Remarks</span></span>

<span data-ttu-id="24782-p102">Ist NumBytes größer als die Anzahl der im Stream-Objekt verbliebenen Bytes, werden nur die verbliebenen Bytes zurückgegeben. Die gelesenen Daten werden nicht aufgefüllt, damit sie der durch NumBytes angegebenen Länge entsprechen. Wenn keine zu lesenden Bytes vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. Mit Read kann nicht rückwärts gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="24782-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="24782-p103">Mit <EM>NumBytes</EM> wird immer die Anzahl an Bytes ermittelt. Verwenden Sie bei aus Text bestehenden <STRONG>Stream</STRONG>-Objekten (<A href="type-property-ado-stream.md">Type</A> ist auf <STRONG>adTypeText</STRONG> festgelegt) die <A href="readtext-method-ado.md">ReadText</A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="24782-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


