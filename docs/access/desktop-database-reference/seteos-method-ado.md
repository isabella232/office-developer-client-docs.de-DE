---
title: SetEOS-Methode (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b45e716844b3e616dfe5b8f94d69f29d6b0f1042
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997511"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="6454d-102">SetEOS-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="6454d-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="6454d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6454d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6454d-104">Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</span><span class="sxs-lookup"><span data-stu-id="6454d-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="6454d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6454d-105">Syntax</span></span>

<span data-ttu-id="6454d-106">*Stream-Objekt*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="6454d-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="6454d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6454d-107">Remarks</span></span>

<span data-ttu-id="6454d-p101">**SetEOS** aktualisiert den Wert der [EOS](eos-property-ado.md)-Eigenschaft, indem sie die aktuelle [Position](position-property-ado.md) als das Ende des Datenstroms festlegt. Alle nach der aktuellen Position folgenden Bytes oder Zeichen werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="6454d-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="6454d-110">Da [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) und [CopyTo](copyto-method-ado.md) keine zusätzlichen Werte in vorhandenen **Stream** -Objekten abschneiden, können Sie diese Bytes oder Zeichen abschneiden, indem Sie diese Position mithilfe von **SetEOS** als neues Ende des Datenstroms festlegen.</span><span class="sxs-lookup"><span data-stu-id="6454d-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="6454d-111">Wenn Sie **EOS** auf eine Position vor dem tatsächlichen Ende des Datenstroms festlegen, gehen alle Daten, die nach der neuen **EOS** -Position folgen, verloren.</span><span class="sxs-lookup"><span data-stu-id="6454d-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>