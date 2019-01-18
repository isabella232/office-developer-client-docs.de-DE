---
title: Read-Methode - ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710888"
---
# <a name="read-method-ado"></a><span data-ttu-id="c244c-102">Read-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="c244c-102">Read method (ADO)</span></span>

<span data-ttu-id="c244c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c244c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c244c-104">Liest eine angegebene Anzahl von Bytes aus einem binären [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c244c-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c244c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c244c-105">Syntax</span></span>

<span data-ttu-id="c244c-106">*Variant* = *Stream-Objekt*. Lesen (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="c244c-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="c244c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c244c-107">Parameters</span></span>

|<span data-ttu-id="c244c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c244c-108">Parameter</span></span>|<span data-ttu-id="c244c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c244c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c244c-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="c244c-110">*NumBytes*</span></span> |<span data-ttu-id="c244c-p101">Optional. Ein **Long** -Wert, der die Anzahl von aus der Datei zu lesenden Bytes oder den [StreamReadEnum](streamreadenum.md)-Wert **adReadAll** angibt. Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c244c-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="c244c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c244c-113">Return value</span></span>

<span data-ttu-id="c244c-114">Die **Read** -Methode liest eine angegebene Anzahl von Bytes oder den gesamten Datenstrom aus einem **Stream** -Objekt und gibt die resultierenden Daten als einen **Variant** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c244c-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c244c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c244c-115">Remarks</span></span>

<span data-ttu-id="c244c-p102">Ist NumBytes größer als die Anzahl der im Stream-Objekt verbliebenen Bytes, werden nur die verbliebenen Bytes zurückgegeben. Die gelesenen Daten werden nicht aufgefüllt, damit sie der durch NumBytes angegebenen Länge entsprechen. Wenn keine zu lesenden Bytes vorhanden sind, wird ein Variant-Wert mit einem Nullwert zurückgegeben. Mit Read kann nicht rückwärts gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c244c-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="c244c-p103">Mit *NumBytes* wird immer die Anzahl an Bytes ermittelt. Verwenden Sie bei aus Text bestehenden **Stream**-Objekten ([Type](type-property-ado-stream.md) ist auf **adTypeText** festgelegt) die [ReadText](readtext-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="c244c-p103">*NumBytes* always measures bytes. For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>


